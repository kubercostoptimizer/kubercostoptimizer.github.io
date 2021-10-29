---
layout: default
title: Implementation
nav_order: 2
has_children: false
permalink: /docs/Implementation
---

## The source code of our framework is available on [GitHub](https://github.com/kubercostoptimizer/Kuber/tree/master/code).
## Docker container with all the dependencies is at [Docker Hub](https://hub.docker.com/r/kuberload/kuber)
---

## Prerequisites for Running
1. Working OpenNebula Cluster: For creating VMs. 
2. Docker Hub Account: Stores app's docker images for Kubernetes to deploy.

---
## Code Structure
The code found in [Github](https://github.com/kubercostoptimizer/Kuber/tree/master/code) is arranged into the following folders:
1. Infrastructure: Handles low-level functions
    - Creates VMs, Kubernetes Cluster, and deploys Istio.
    - Deploys combinations onto VM types.
    - Uses OpenNebula and Kubernetes APIs to work.
2. Profiler: Executes a combination on a VM type
    - Creates initial cluster needed for all services in the app.
    - Uses Infrastructure to place the combination on the test VM.
    - Loads the databases for the app.
    - Load tests the app and extracts performance data from Istio logs. 
3. Kuber:
    - Code for Combination selector and Deployment Planner.
4. SSOT: Configuration 
    - Information about VM types and services.
5. Apps
    - Application deployment files and load tests.

---
### Configuration

Kuber needs the following information from the application developer:

#### Data about the application

1. We need Kubernetes deployment files (.yamls) for deploying services and their dependencies.
   - place all the deployment files in /apps/app_name/deploy folder.
2. Load test that needs to be executed to test a combination
   - copy existing load_test folder from /apps/sock-shop/load_test
   - update /apps/app_name/load_test/locustfile.py with required test scenario.
3. Initial configuration such as loading databases
   - create a folder apps/app_name/load_test/init_scripts/
   - place the required code and invoke it with script run.sh

#### SSOT: Single Source Of Truth

Application developers have to configure VM types and services that need to be tested in file SSOT/config.json.
Example config.json file in SSOT folder:

``` json
{
  "Application": 
      {
          "name": "app_name",
          "services": ["service1", "service2"],
          "front-end": "service1",
          "port": "5000"
      },
  "Profiling":
      {
        "load_gen":
          {
           "time_limit":"2m",
           "concurrent":"100"
          }
      },
  "Infrastructure":
      {
        "Cloud_provider": "opennebula",
        "vm_types":[
                {
                  "name"          : "m4.large",
                  "cpu_count"     : "2",
                  "ram"           : "8",
                  "computer"      : "leibnitz",
                  "price"         : 0.10
                },
                {
                  "name"          : "m4.xlarge",
                  "cpu_count"     : "4",
                  "ram"           : "16",
                  "computer"      : "leibnitz",
                  "price"         : 0.20
                },
              ]
      }
}
```
Below we explain in detail each of the config options:
1. Application
   - name: Name of the application, should be same as the namespace given in Kubernetes deployment files, and folder name in /apps.
   - services: names of each microservice, should be the same as Kubernetes services in /apps/app_name/deploy.
   - front-end: service that receives external traffic into the application.
   - port: port exposed by front-end.
2. Profiling 
   - time_limit: the amount of time to run a load test.
   - concurrent: number of concurrent users that run the test.
3. VM types
   - Each entry in this list corresponds to a VM type
   - name: user-given name for the VM type
   - cpu_count: number of CPU cores
   - ram: RAM size in GB
   - computer: physical machine to place the VM type in. Hostname in OpenNebula cluster. 
   - price: cost per hour in $.
   
---
### Running the Kuber with Docker container
1. Download the docker container from the [Docker Hub](https://hub.docker.com/r/kuberload/kuber) and the code from [GitHub](https://github.com/kubercostoptimizer/Kuber/tree/master/code).
2. Run the docker container with code using the following command:
```sh
docker run -it -v /code:/wd/code kuberload/kuber:latest /bin/bash
```
3. Then execute the Kuber inside the container:
```sh
cd /wd/code/kuber
python run.py
```
