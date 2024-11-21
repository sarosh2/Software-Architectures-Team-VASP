# ADR: Multi-Tiered Fault Tolerance for FMMS

## Decision
We will implement a multi-tiered fault-tolerance and availability strategy for the Flood Monitoring and Management System which includes the following key tactics:

## Tactics
1. **Redundancy**: Deploy redundant sensors and subsystems in critical areas to ensure that if one sensor fails, others can continue to provide data. This includes using multiple types of sensors (e.g., water level, rainfall) distributed throughout the flood-prone areas to minimize single points of failure.
2. **Data Replication**: Utilize data replication strategies across multiple geographic locations. This will ensure that all critical data collected from the sensors are stored in multiple databases or data stores. In case of network failure or hardware malfunctions at one location, the system can access replicated data from another site.
3. **Failover Handling**: Implement automatic failover mechanisms for the communication subsystems. This includes setting up backup communication channels (e.g., cellular, satellite) to ensure continuous data transmission even when the primary communication mode is disrupted.
4. **Load Balancing**: Integrate load balancing techniques to distribute processing loads among multiple nodes. This will help in managing high data loads and prevent overloading any single service, thereby maintaining system responsiveness.
5. **Graceful Degradation**: Design the system to allow for graceful degradation of service. In scenarios where certain functionalities are impaired (for instance, loss of real-time data), the system should still be able to provide historical data and issue alerts without complete functionality loss.
## Consequences
- **Positive Consequences**: 
•	Increased system reliability and availability during adverse conditions.
•	Reduced risk of data loss through redundancy and replication.
•	Enhanced responsiveness to failures with automated failover handling.
•	Ability to handle high data volumes without service degradation through load balancing.

- **Negative Consequences**:
•	Increased complexity in system design and architecture due to multiple redundancy and failover mechanisms.
•	Additional operational costs associated with maintaining multiple hardware and communication infrastructures.
•	Potential challenges in synchronizing data across replicated systems, requiring thorough testing and monitoring processes.

