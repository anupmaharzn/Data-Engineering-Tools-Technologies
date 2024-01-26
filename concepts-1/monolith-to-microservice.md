# Monolith TO MicroServices

## Monolithic vs Microservice

| Monolicthic | Microservice| 
| :---:   | :---: | 
| All components tightly coupled into single,cohesive unit.| This architectural approach creates a larger application out of multiple modular services that communicate via APIs   | 
| one code base and runtime environment to create a single-tiered application | loosly coupled,independently deployable services use independent databases and coding  |

![Capture](https://github.com/anupmaharzn/Data-Engineering-Tools-Technologies/assets/34486226/6acf12ea-ec37-4f7a-bbde-c52c23a4c7ca)

### advantage of Microservice over Monolith
- faster delivery
- isolation
- scaling
- flexibility

### But Microservice also comes with challenges
- servie discovery
- load balancing
- fault tolerance
- distributed tracing
- security(TLS,polices,patches)
- Note ```each microservice might be running in different machines or VMs (How on services knows the ip address of another service? (how to locate?))```
    - `you might be thinking to hardcode the ip address but in cloud if your VMs restart or have multiple copy of instance it will have different Ip addresss.`
    - Solution
    ![service discovery 1](https://github.com/anupmaharzn/Data-Engineering-Tools-Technologies/assets/34486226/1036c1d2-db28-41be-965c-ac2486cfc008)
    - but another problem statements
    ![service discovery 2](https://github.com/anupmaharzn/Data-Engineering-Tools-Technologies/assets/34486226/f307bc3d-f600-46a9-9101-57fe4bd38562)
    - solution
    ![service discovery 3](https://github.com/anupmaharzn/Data-Engineering-Tools-Technologies/assets/34486226/368fd07d-37d6-471e-880b-66a8cd44167d)



## Service mesh
- concept that applies to microservices
- service mesh intent to solve this microservice challenges
- ``Motto`` Dont burden my code with all these infrastructure related decisions.

![service mesh 1](https://github.com/anupmaharzn/Data-Engineering-Tools-Technologies/assets/34486226/bd02d6d4-4f5e-4eaf-a27e-64c3b4bb4ad3)

- sidecar is program(is an proxy)
- sidecar is offloading all the communication related heavy lifting from the code(service code)

![service mesh 2](https://github.com/anupmaharzn/Data-Engineering-Tools-Technologies/assets/34486226/eb38ad05-3aef-4b88-a484-93d30665c407)

- control tower could be program to manage sidecar.
-control tower is responsible for  pushing insturction like (policies,certs,configs etc)

![service mesh 3](https://github.com/anupmaharzn/Data-Engineering-Tools-Technologies/assets/34486226/65906be4-4673-44b8-a66d-d2a8b076a15f)

- gRPC is communication protocol between sidecars of service A and service B


```This whole concept of sidecar and control tower is service mesh(mechanism for managing communications between the various individual services that make up mordern application in a microservice-based system)```
