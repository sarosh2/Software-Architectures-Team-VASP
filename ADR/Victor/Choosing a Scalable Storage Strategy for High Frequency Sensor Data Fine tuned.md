#  Choosing a Scalable Storage Strategy for High Frequency Sensor Data Fine tuned

## Status
Proposed

## Context

The Flood monitoring and Management system will receive continuous data 
from up to 150,000 sensors. To handle this large volume, the system needs a storage 
approach that can support rapid data ingestion, quick retrieval, and long-term scalability 
as the number of sensors grows. The chosen strategy must accommodate the 
high-frequency nature of data updates while ensuring efficient performance under peak 
loads.

## Decision

[Proposed Design Scenario]****: [What is the change that we're proposing and/or doing]
The proposed design focuses on moving data from source to destination using the Apache Kafka protocol. This approach allows for high-frequency data updates without requiring any sort of aggregation or processing at the Sensor connector or at the Flood SSC. The design includes three main components:\n1. A large Kafka topic will ingest all flood event data from up to 150,000 sensors.