#### Spark Applications

* Spark Applications consist of a <b>driver</b> process and a set of <b>executor</b> processes. 

* The driver process runs your main() function, sits on a node in the cluster, and is responsible for three things:

1. maintaining information about the Spark Application; 
2. responding to a user’s program or input; and
3. analyzing, distributing, and scheduling work across the executors (discussed momentarily). 

* The <b>driver</b> process is absolutely essential—it's the heart of a Spark Application and maintains all relevant information during the lifetime of the application.

* The <b>executors</b> are responsible for actually carrying out the work that the driver assigns them. 

* This means that each executor is responsible for only two things: 

1. executing code assigned to it by the driver, and 
2. reporting the state of the computation on that executor back to the driver node.
