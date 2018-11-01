#### Partitions
* To allow every executor to perform work in parallel, Spark breaks up the data into chunks called <b>partitions</b>. 
* A partition is a collection of rows that sit on one physical machine in your cluster. 
* A DataFrame's partitions represent how the data is physically distributed across the cluster of machines during execution. 
* If you have one partition, Spark will have a parallelism of only one, even if you have thousands of executors. 

* If you have many partitions but only one executor, Spark will still have a parallelism of only one because there is only one computation resource.
* An important thing to note is that with DataFrames you do not (for the most part) manipulate partitions manually or individually. 

* You simply specify high-level transformations of data in the physical partitions, and Spark determines how this work will actually execute on the cluster. Lower-level
APIs do exist (via the RDD interface)
