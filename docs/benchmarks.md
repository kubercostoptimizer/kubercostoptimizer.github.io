---
layout: default
title: Benchmarks
nav_order: 3
has_children: false
permalink: /docs/benchmarks
---

# Benchmarks Used in Evaluation
---

In this section, we provide details about benchmark applications used in Kuber evaluvation.
We added traces to each API in the application to calculate execution time of the API while excluding the Response time.

In table below, we present original and modified versions of code for each benchmark.

|Benchmark Name|Number of Services| Orginal Repo | Changed Repo|
|:-------------------------------|:------------------:|
|Social Network|12|[link](https://github.com/delimitrou/DeathStarBench/tree/master/hotelReservation)|[link](https://github.com/kubercostoptimizer/Kuber/tree/master/code/apps/social-network/code)
|Media Microsvc|11|[link](https://github.com/delimitrou/DeathStarBench/tree/master/mediaMicroservices)|[link](https://github.com/kubercostoptimizer/Kuber/tree/master/code/apps/media-microsvc/code)
|Hotel Reservation|8|[link](https://github.com/delimitrou/DeathStarBench/tree/master/hotelReservation)|[link](https://github.com/kubercostoptimizer/Kuber/tree/master/code/apps/hotel-reservation/code)
|Sockshop|7|[link](https://github.com/microservices-demo)|[link](https://github.com/kubercostoptimizer/Kuber/tree/master/code/apps/sock-shop/code)


Example of instrumented code for Get API in Catalogue service of SockShop:
``` go
 
 // Original API definition
func (s *catalogueService) Get(id string) (Sock, error) {   
        // other code
        err := s.db.Get(&sock, query, id)
        // other code
        return sock, nil
}
 
 // API definition with execution time calculations 
func (s *catalogueService) Get(id string) (Sock, error) {
      start := time.Now() // <- Start Timer for API Total Execution time
      elapsed_external_call_time := time.Duration(0)
      span := opentracing.StartSpan("Get")

      // Other code
 
      external_call_2 := time.Now()
      err := s.db.Get(&sock, query, id)  // <- External Call
      elapsed_external_call_time = elapsed_external_call_time + time.Since(external_call_2)

      // Other code
      
      elapsed := time.Since(start) // <- end Timer for API Total Execution time
      elapsed = elapsed - elapsed_external_call_time
      span.LogKV("runtime_ms",float64(elapsed)/float64(time.Millisecond)) // <- send data to Istio
      span.Finish()
      return sock, nil
}

```

