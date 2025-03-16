# Big Data Ecosystem & HDFS Quiz

## Multiple Choice Questions 

### 1. According to the CAP theorem, a distributed data system can only guarantee:

- All three properties: Consistency, Availability, and Partition Tolerance
- Consistency and Availability, but not Partition Tolerance
- Availability and Partition Tolerance, but not Consistency
- Two of the three properties at any given time

**Answer: Two of the three properties at any given time**

### 2. In the context of HDFS architecture, what is the primary role of the NameNode?

- Manages the local storage attached to individual nodes
- Performs block creation, deletion, and replication
- Manages the filesystem namespace and regulates access to files
- Connects multiple racks through network switches

**Answer: Manages the filesystem namespace and regulates access to files**

### 3. Which of the following is NOT a characteristic of HDFS?

- Suitable for low-latency data access
- Fault tolerance through data replication
- Designed for large files and batch processing
- High throughput access to application data

**Answer: Suitable for low-latency data access**

### 4. What happens during the SafeMode startup phase in HDFS?

- Data blocks are deleted and recreated
- Replication of data blocks does not occur
- The NameNode is temporarily shut down
- DataNodes are prevented from sending heartbeats

**Answer: Replication of data blocks does not occur**

### 5. What is the primary difference between ACID and BASE properties in the context of database systems?

- ACID scales horizontally while BASE scales vertically
- ACID allows multiple applications to update the same record simultaneously while BASE does not
- ACID ensures synchronization at the database level while BASE does not
- BASE processes large volumes of data more efficiently than ACID

**Answer: ACID ensures synchronization at the database level while BASE does not**

### 6. In HDFS, what determines the optimal placement of data block replicas?

- Random distribution to ensure even load
- Rack-aware placement to optimize reliability and bandwidth
- Alphabetical ordering of DataNode names
- Size of the data blocks

**Answer: Rack-aware placement to optimize reliability and bandwidth**

### 7. Which of the following is NOT a challenge that traditional RDBMS faces when dealing with Big Data?

- Handling unstructured data efficiently
- Horizontal scaling capabilities
- Maintaining ACID properties
- Processing high-velocity data streams

**Answer: Maintaining ACID properties**

### 8. What is the primary function of the EditLog in HDFS?

- It stores the mapping of blocks to files
- It records every change that occurs to the filesystem metadata
- It keeps track of corrupted data blocks
- It manages the replication factor of data blocks

**Answer: It records every change that occurs to the filesystem metadata**

### 9. What is the default replication strategy for HDFS with a replication factor of 3?

- All replicas are stored on the same DataNode
- One replica on the local rack, two on different racks
- One replica on a node in the local rack, one on a different node in the local rack, and one on a node in a different rack
- All replicas are stored on different racks

**Answer: One replica on a node in the local rack, one on a different node in the local rack, and one on a node in a different rack**

### 10. Which of the following statements about HDFS is FALSE?

- It supports multiple concurrent writers to the same file
- It is designed for batch processing rather than real-time data access
- It allows for the creation of hierarchical file systems with directories
- It can detect and recover from data corruption using checksums

**Answer: It supports multiple concurrent writers to the same file**

## True/False Questions

### 11. HDFS is an ideal solution for storing many small files.

- True
- False

**Answer: False** (HDFS is not good for many small files as it creates scalability issues for the NameNode)

### 12. The BASE model prioritizes consistency over availability in distributed systems.

- True
- False

**Answer: False** (BASE prioritizes availability over consistency, offering "eventual consistency")

### 13. In HDFS, the NameNode maintains the entire filesystem namespace in memory.

- True
- False

**Answer: True** (The NameNode keeps the image of the entire filesystem namespace and file Blockmap in memory)

### 14. DataNodes in HDFS have knowledge about the overall filesystem structure.

- True
- False

**Answer: False** (DataNodes have no knowledge about the HDFS filesystem; they simply store data blocks)

### 15. The CAP theorem was proposed by Eric Brewer in 2000.

- True
- False

**Answer: True** (As stated in the document, the CAP theorem was proposed by Eric Brewer in 2000)

### 16. HDFS supports a write-once-read-many (WORM) access model.

- True
- False

**Answer: True** (HDFS applications need a write-once-read-many access model for files)

### 17. The Apache Hadoop framework was named after its creator's pet dog.

- True
- False

**Answer: False** (It was named after the creator's son's toy elephant)

### 18. The Secondary NameNode in HDFS provides automatic failover if the primary NameNode fails.

- True
- False

**Answer: False** (The Secondary NameNode does not provide automatic failover; the NameNode remains a single point of failure)

### 19. HDFS allows data blocks to be updated in place after they are written.

- True
- False

**Answer: False** (HDFS follows a write-once model where blocks cannot be updated in place after writing)

### 20. RDBMS typically relies on horizontal scaling while Big Data systems rely on vertical scaling.

- True
- False

**Answer: False** (It's the opposite: RDBMS typically relies on vertical scaling while Big Data systems rely on horizontal scaling)
