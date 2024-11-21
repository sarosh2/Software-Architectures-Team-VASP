# Choosing a Scalable Storage Strategy for High-Frequency Sensor Data 

## rejected

## The Flood monitoring and Management system will receive continuous data from up to 150,000 sensors. To handle this large volume, the system needs a storage approach that can support rapid data ingestion, quick retrieval, and long-term scalability as the number of sensors grows. The chosen strategy must accommodate the high-frequency nature of data updates while ensuring efficient performance under peak loads. What is the best storage architecture to support a high-volume, high-frequency data ingestion system for the above case. Give opinion about different SA Styles with reasons that can support this kind of requirement

## We will use a Disks + Storage Service architecture. It brings together the best of both worlds: the reliability andcejility of running the precious data on disk, along with the scalability and irresponsibility of a storage service. It also addresses the problem of both cost and capacity by allowing the service to automatically scale up to 150,000 sensors. The disks provide junior storage, while the storage service provides the senior storage. Hence, this architecture meets the Flood HMS requirements of data integrity,
