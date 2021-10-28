---
layout: default
title: Benchmarks
nav_order: 3
has_children: false
permalink: /docs/benchmarks
---

# Benchmarks Used in Evaluation
---

Within this section, we provide the our benchmark applications we used to evaluvate Kuber.
We added traces to each API in the application to calculate execution time of the API while excluding the Response time.
Example of instrumented code:
``` java
 
 // Original API definition
 public Cart get(@PathVariable String customerId) {
        return new CartResource(cartDAO, customerId).value().get();
 }
 
 // API definition with execution time calculations 
  public Cart get(@PathVariable String customerId) {
      long startTime = System.nanoTime();
      final Span span = tracer.buildSpan("get_cart").start();
      Cart obj = new CartResource(cartDAO, customerId).value().get();
      long duration = System.nanoTime() - startTime;
      HashMap hm = new HashMap();
      hm.put("runtime_ms",duration/1000);
      System.out.println("get call took "+duration);
      span.log(hm);
      span.finish();
      return obj;
  }

```
In below table, we present original and modified versions of code for each benchmark.

|Benchmark Name|Number of Services| Orginal Repo | Changed Repo|
|:-------------------------------|:------------------:|
|Social Network|12|[link](https://github.com/delimitrou/DeathStarBench/tree/master/hotelReservation)|[link](https://github.com/kubercostoptimizer/Kuber/tree/master/code/apps/social-network/code)
|Media Microsvc|11|[link](https://github.com/delimitrou/DeathStarBench/tree/master/mediaMicroservices)|[link](https://github.com/kubercostoptimizer/Kuber/tree/master/code/apps/media-microsvc/code)
|Hotel Reservation|8|[link](https://github.com/delimitrou/DeathStarBench/tree/master/hotelReservation)|[link](https://github.com/kubercostoptimizer/Kuber/tree/master/code/apps/hotel-reservation/code)
|Sockshop|7|[link](https://github.com/microservices-demo)|[link](https://github.com/kubercostoptimizer/Kuber/tree/master/code/apps/sock-shop/code)
