# Monolith TO MicroServices

## Monolithic vs Microservice

| Monolicthic | Microservice| 
| :---:   | :---: | 
| All components tightly coupled into single,cohesive unit.(one code base and runtime environment to create a single tiered application) | This architectural approach creates a larger application out of multiple modular services that communicate via APIs(loosly coupled,independently deployable services use independent databases and coding)   | 
| :---:   | :---: | 
| Seconds | 301   |

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
Note each microservice might be running in different machines or VMs (How on services knows the ip address of another service? (how to locate?))
    - you might be thinking to hardcode the ip address but in cloud if your VMs restart or have multiple copy of instance it will have different Ip addresss.

## Service mesh
- concept that applies to microservices
- service mesh intent to solve this microservice challenges
- ``Motto`` Dont burden my code with all these infrastructure related decisions.

### image

- sidecar is program(is an proxy)
- sidecar is offloading all the communication related heavy lifting from the code(service code)

### image 2

- control tower could be program to manage sidecar.
-control tower is responsible for  pushing insturction like (policies,certs,configs etc)

### image 3

- gRPC is communication protocol between sidecars of service A and service B


```This whole concept of sidecar and control tower is service mesh(mechanism for managing communications between the various individual services that make up mordern application in a microservice-based system)```
