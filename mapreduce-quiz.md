# MapReduce Programming Model Quiz

## Multiple Choice Questions

1. Who led the conception and design of Google's MapReduce framework?
   - Jeffrey Dean and Sanjay Ghemawat
   - Doug Cutting and Mike Cafarella
   - Hadoop and Apache
   - Larry Page and Sergey Brin

   **Answer: Jeffrey Dean and Sanjay Ghemawat**

2. Which of the following is NOT a characteristic of MapReduce?
   - Parallel Processing
   - Fault Tolerance
   - Real-time Processing
   - Data Locality Optimization

   **Answer: Real-time Processing**

3. In MapReduce, what does the Record Reader component do?
   - It reads the configuration files for the job
   - It converts the physical representation of the input data into key-value pairs for the mapper
   - It stores the intermediate output on local disk
   - It splits the input file into chunks for distributed processing

   **Answer: It converts the physical representation of the input data into key-value pairs for the mapper**

4. What is the primary role of the Combiner in MapReduce?
   - To combine the output of multiple mappers before sending to reducers
   - To perform global aggregation on the final output
   - To combine the output of multiple reducers
   - To perform local aggregation on the output of mappers before sending to reducers

   **Answer: To perform local aggregation on the output of mappers before sending to reducers**

5. Which component in MapReduce is responsible for determining which reducer should receive a particular key-value pair?
   - InputSplit
   - Partitioner
   - Shuffler
   - OutputFormat

   **Answer: Partitioner**

6. What is the formula used to calculate the split size in MapReduce?
   - splitSize = max(minSplitSize, min(maxSplitSize, blockSize))
   - splitSize = min(minSplitSize, max(maxSplitSize, blockSize))
   - splitSize = average(minSplitSize, maxSplitSize, blockSize)
   - splitSize = sum(minSplitSize, maxSplitSize, blockSize) / 3

   **Answer: splitSize = max(minSplitSize, min(maxSplitSize, blockSize))**

7. Which of the following is NOT a type of InputFormat in MapReduce?
   - TextInputFormat
   - KeyValueTextInputFormat
   - XMLInputFormat
   - GraphInputFormat

   **Answer: GraphInputFormat**

8. Which process is responsible for transferring data from the mappers to the reducers in MapReduce?
   - Splitting
   - Partitioning
   - Shuffling and Sorting
   - Merging

   **Answer: Shuffling and Sorting**

9. In MapReduce, what is the recommended number of reducers according to the document?
   - Equal to the number of nodes in the cluster
   - Equal to the number of mappers
   - 0.95 or 1.75 multiplied by (<no. of nodes> * <no. of maximum containers per node>)
   - One reducer per 128MB of data

   **Answer: 0.95 or 1.75 multiplied by (<no. of nodes> * <no. of maximum containers per node>)**

10. Which of the following is an example of a Meta Pattern in MapReduce?
    - Inverted Index
    - Numerical Summarization
    - Job Chaining
    - Distinct Filtering

    **Answer: Job Chaining**

11. What happens during the "Shuffling" phase in MapReduce?
    - Data is partitioned into different groups
    - Output from mappers is sorted and transferred to reducers
    - Reducers execute their functions on the data
    - Input data is split into chunks for parallel processing

    **Answer: Output from mappers is sorted and transferred to reducers**

12. Which of the following statements about the Mapper in MapReduce is FALSE?
    - Mapper processes each input record and generates a new key-value pair
    - One mapper is created for each InputSplit
    - Mapper output is stored on HDFS
    - Mapper can generate completely different key-value pairs from the input

    **Answer: Mapper output is stored on HDFS**

13. What is the primary function of the RecordReader in MapReduce?
    - To read the input file and split it into chunks
    - To convert InputSplit into key-value pairs for the mapper
    - To read configuration files for the job
    - To combine the output of multiple mappers

    **Answer: To convert InputSplit into key-value pairs for the mapper**

14. Which join pattern in MapReduce can take the longest time to execute but supports all different join operations?
    - Replicated Join
    - Composite Join
    - Reduce Side Join
    - Cartesian Product

    **Answer: Reduce Side Join**

15. What is the formula to calculate the number of mappers in a MapReduce job?
    - Number of mappers = Number of nodes in the cluster
    - Number of mappers = (total data size) / (input split size)
    - Number of mappers = Number of reducers * 2
    - Number of mappers = Number of blocks in HDFS

    **Answer: Number of mappers = (total data size) / (input split size)**

16. Which of the following is NOT a summarization pattern in MapReduce?
    - Numerical Summarization
    - Counting with Counters
    - Inverted Index
    - Total Order Sorting

    **Answer: Total Order Sorting**

17. In the context of MapReduce, what does the "Partitioner" component do?
    - It partitions the input data into chunks for processing
    - It splits the input file into logical InputSplits
    - It assigns each key to a specific reducer
    - It divides the output into multiple files

    **Answer: It assigns each key to a specific reducer**

18. Which component in MapReduce is responsible for performing the final aggregation of the results?
    - Mapper
    - Combiner
    - Reducer
    - OutputFormat

    **Answer: Reducer**

19. What is the difference between a Replicated Join and a Reduce Side Join in MapReduce?
    - Replicated Join is executed on the map side with one large dataset and several small datasets
    - Replicated Join is executed after the reduce phase
    - Replicated Join combines records from different mappers
    - Replicated Join produces more intermediate data than Reduce Side Join

    **Answer: Replicated Join is executed on the map side with one large dataset and several small datasets**

20. Which of the following components in a MapReduce application is mandatory?
    - Mapper and Driver
    - Reducer and Combiner
    - Partitioner and RecordReader
    - OutputFormat and Combiner

    **Answer: Mapper and Driver**

## True/False Questions

1. - In MapReduce, the combiner is also known as the "Mini-reducer".
   **Answer: True**

2. - The default number of reducers in a MapReduce job is 3.
   **Answer: False** (The default is 1)

3. - The output of the mappers in MapReduce is always stored on HDFS.
   **Answer: False** (It's stored on local disk)

4. - In MapReduce, the Partitioner component ensures that all values for a single key go to the same reducer.
   **Answer: True**

5. - The TextInputFormat is the default InputFormat for MapReduce jobs.
   **Answer: True**

6. - A MapReduce job can have multiple mappers but only one reducer.
   **Answer: False** (It can have multiple reducers)

7. - The Job Merging pattern in MapReduce allows two related jobs to share the same MapReduce pipeline.
   **Answer: False** (It allows two unrelated jobs to share the pipeline)

8. - The Cartesian Product pattern in MapReduce is efficient and should be used for large datasets.
   **Answer: False** (It can take an extremely long time to complete)

9. - In MapReduce, the RecordReader communicates with the InputSplit until the file reading is completed.
   **Answer: True**

10. - The Shuffling pattern in MapReduce is designed to maintain the order of data in records.
    **Answer: False** (It's designed to completely randomize the records)
