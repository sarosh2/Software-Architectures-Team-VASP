# Context
Flood Monitoring and Management System (FMMS) involves multiple components—data ingestion, processing, alerting, and user management—that may evolve independently over time. For flexibility in development, deployment, and maintenance, the architecture needs a modular design that enables isolated updates, scalability, and troubleshooting for individual components without impacting the entire system. The architecture style must support this modularity, allowing FMMS to adapt to future requirements and updates efficiently. which style should we should use to have minimal interdependencies and promote modular architecture ?
## Status
rejected
## Decision:
 We will adopt the Microservices architecture for FMMS. In this architecture, multiple services (some of which are optional) are deployed as individual services with a service-to-service communication protocol (such as HTTP) in a services communication graph. <sup>[1]</sup>scopes of the services are restricted to their respective functions, with no shared data stores. Services are independent of each other and are never mechanically coupled. Instead, they communicate through explicit and intentional APIs between services. A service

