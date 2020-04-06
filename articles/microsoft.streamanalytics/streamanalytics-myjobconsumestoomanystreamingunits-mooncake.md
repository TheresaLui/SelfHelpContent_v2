<properties 
	pageTitle="My job consumes too many streaming units"
	description="My job consumes too many streaming units"
	service="microsoft.streamanalytics"
	resource="streamingjobs"
	authors="samacha"
	displayOrder="3"
	selfHelpType="resource"
	supportTopicIds=""
	productPesIds=""
	cloudEnvironments="MoonCake"
	articleId="6e565303-3332-4605-b296-275d5143c2d8"
	ownershipId="AzureData_StreamAnalytics"
/>

# My job consumes too many streaming units

## **Recommended steps**
Streaming units (SUs) represent the computing resources consumed to execute an Azure Stream Analytics job. SUs provide a way to describe the relative event processing capacity based on a blended measure of CPU, memory, and read and write rates.

Choosing how many SUs are required for a particular job is depends on the on the partition configuration for the inputs and the query defined for the job. The Scale blade allows the setting of the right amount of Scale Units needed.  

It is a best practice to allocate more Streaming Units than needed. The ASA processing engine optimizes for latency and throughput at the cost of using additional memory. [More about Scalability and configuring your job to scale](https://docs.azure.cn/stream-analytics/stream-analytics-scale-jobs) 

In general, it is a best practice to start with 6 Streaming Units for queries not using PARTITION BY, and determine the sweet-spot using a trial and error method by suitably modifying the number of streaming units after passing representative amounts of data and examining the SU %Utilization metric. 

Azure Stream Analytics keeps events in a window called the “reorder buffer” before starting any processing. Events are sorted inside the reorder window by time and subsequent operations are performed on the temporally sorted events. Reordering events by time ensures that the operator has visibility into all of the events in the stipulated timeframe, thereby allowing it to perform the requisite processing and produce an output. A side effect of this mechanism is that processing is delayed by the duration of the reorder window. The memory footprint of the job (which affects Streaming Unit consumption) is a function of the size of this reorder window and number of events contained in it. 

The most common causes of high memory utilization that contributes to high streaming unit usage for jobs include 

_1) High cardinality for GROUP BY_

The cardinality of incoming events dictates memory usage for the job. 

For example, in `Select count(*) from input group by clustered, tumblingwindow (minutes, 5)` the number associated with clustered is the cardinality of the query. 

In order to ameliorate issues caused by high carnality, scale out query by increasing partitions using the Partition By as shown: 

~~~~
Select count(*) from input 
partition by clusterid 
group by clustered tumblingwindow (minutes, 5)
~~~~

The number of `clustered` is the cardinality of GROUP BY here.

Once the query is partitioned out, it is spread out over multiple nodes. As a result, the number of events coming into each node is reduced thereby reducing the size of the reorder buffer. Eventhub partitions should also be partitioned by partitionid.

_2) High unmatched event count for Join_

The number of unmatched events in the join affect the memory unitization for the query. The following query is looking to find the ad impressions that generate clicks: 

~~~~
SELECT id from clicks INNER JOIN,
impressions on impressions.id = clicks.id AND DATEDIFF(hour, impressions, clicks) between 0 AND 10
~~~~

It is possible that lots of ads are shown and few people click on it and it is required to keep all the events in the timewindow. Memory consumed is proportional to the window size and event rate. 

To remediate this, scale out query by increasing partitions using the partition by. 

Once the query is partitioned out, it is spread out over multiple nodes. As a results the number of events coming into each node is reduced thereby reducing the size of the reorder buffer.  

_3) Large number of out of order events_ 

A large number of out of order events in a large time window will cause the size of the "reorder buffer" to be larger. To remediate this, scale out query by increasing partitions using the partition by. Once the query is partitioned out, it is spread out over multiple nodes. As a results the number of events coming into each node is reduced thereby reducing the size of the reorder buffer.  

_Open a Microsoft Support case_ 

If you are still not able to figure out what is going on, then go to operations log, select one of the latest entries and click Details button and copy all the details on that page and use that info to supply to Microsoft Support. 

Additionally, if possible include sample data from a time when the job was expected to produce output.  
