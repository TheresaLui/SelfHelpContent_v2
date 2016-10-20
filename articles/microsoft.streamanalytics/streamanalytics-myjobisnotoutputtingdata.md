<properties 
    pageTitle="My job is not outputting data"
    description="My job is not outputting data"
    service="microsoft.streamanalytics"
    resource="streamingjobs"
    authors="kschaefer13"
    displayOrder="1"
    selfHelpType="resource"
	supportTopicIds=""
    productPesIds=""
    cloudEnvironments="public"
/>

# My job is not outputting data

## **Recommended steps**

1. Verify connectivity to inputs and outputs by using the "Test Connection" button for each of the inputs and outputs. 
2. Use "Service Bus Explorer" to connect to Azure EventHub (if EventHub input is used) to verify that input data is flowing into EventHub.
3. Use the "Sample Data" button for each of the inputs and download the input sample data. 
4. Inspect the sample data to understand the shape of the data: the schema, and the data types. 
5. On the Query tab, use the "Test" button to test the query and use the sample data downloaded to test the query. Examine any errors and attempt to remediate them.
6. If Timestamp By is used, make sure the events have timestamps greater than the job start time. 
7. Re-build the query progressively from simple select statement to more complex aggregates using steps. Using `WITH` clause to build up the query logic, step by step. It's is possible that their query is functioning just fine but for example, a where clause in the query filtered out their events that prevented outputs from being generated. 
8. If all these steps worked fine, go to Settings blade and pick event ordering. Make sure this policy is configuration makes sense for your job. It should be noted that this policy is not applied when the "Test" button is used to test the query. This is a difference between testing in browser verses running the job for real. 
9. Start the Job and check if the job works as desired.  
10. Once the job status changes to "Running", depending on the duration stipulated in the query, the output can be seen in the Sink data-source. 
11. If no output is obtained after the expected duration (based on the query), try the following: <br>
    * a. Look at Monitoring Metrics on Monitor tab. The metrics here are delayed by about couple of minutes as they are aggregated values over last minute. <br>
    * b. Look at the metrics for Input Events, Runtime Errors, Data Conversion Errors. <br>
        * If Input Events > 0, the ASA job is able to read data. If not, then the problems may be <br>
            * Look at the data source and see if it has valid data for this job using Service Bus Explorer (if Event Hub is used as input) <br>
            * Check if the Data serialization format and Encoding are as expected. <br>
            * If using Event Hub, the Body of the Message may be Null. <br>
        * If Data Conversion Errors > 0 and climbing, that means: <br>
            * Job may not be able to deserialize the events. <br>
            * Events schema may not match the defined/expected schema of the events in the query. <br> 
            * DataType of some of the fields in the Event may not be what is expected. Test with sample data to confirm working. <br>
        * If Runtime Errors > 0, means that the ASA Job is able to receive the data but is getting errors while processing the query. Go to the Operation Logs and filter on "Failed" status to find all these errors. <br>
        * If InputEvents > 0 and OutputEvents = 0, means one of the following: <br>
            * Query processing resulted in zero output events. <br>
            * Events or its fields may be malformed, so resulted in zero output after query processing. 3. Unable to push data to Output Sink for connectivity/authentication reasons. <br>
        * In all these error cases, Operations Log messages explain additional details (including what is happening), except for the cases the query logic filtered out all events. If the processing of multiple events generates errors, Stream Analytics logs the first 3 error messages of the same type within 10 minutes to Operations logs and then suppress additional identical errors with a message that reads "Errors are happening too rapidly, these are being suppressed". <br> 

When outputs going to a specific output type are not seen, redirect the output to different output type that is less complex (such as Azure Blobs) and check if the output can be seen up there (using Storage Explorer). 

If there are no issues, the data flow will need to be analyzed. Analyzing the data flow systematically can be done with the job diagram that shows a visual representation of the job by clicking on the "Job diagram" button in the "Settings" blade of the of the Stream Analytics job. For existing jobs, it is necessary to restart the job first. 

Every input and output is color coded to indicate the current state of that component. 

To look at intermediate query steps to understand the data flow patterns inside stream analytics, the visualization tool provides a view of the breakdown of the query into its component steps and the flow sequence. Each logical node shows the number of partitions it has.  

Clicking on each query step will show the corresponding section in a query editing pane as illustrated. A metrics chart for the step is also displayed in a lower pane. 

Clicking the … will pop up the context menu allowing the expansion of partitions showing the partitions of the Event Hub input in addition to the input merger. 

Clicking a single partition node will show the metrics chart only for that partition on the bottom. 

Selecting the merger node will show the metrics chart for the merger. The chart below shows that no events got dropped or adjusted. 

Additionally, hovering on the chart will show details of the metric value and time.

In the job diagram, examine the following input metrics to help answer the following targeted questions about jobs getting data from its input sources. If the query is partitioned, examine each partition.  

**QueryLastProcessedTime** This metric indicates when a particular step received data. Based on the topology, work backwards from the output processor to see which step is not receiving data. If a step is not getting data, go to the preceding step is a query step, check if it has a time window and if enough time has passed for it to output data (Note that time windows are snapped to the hour). 

If the preceding step is an input processor, use the input metrics to help answer the following targeted questions about jobs getting data from its input sources. If the query is partitioned, examine each partition.  

_1) How much data is actually being read?_ 

**InputEventsSourcesTotal** metric provides the number of data units read, eg number of blobs. <br>
**InputEventsTotal** provides the number of events read. This metric is available per partition. <br>
**InputEventsInBytesTotal** provides the number of bytes read. <br>
**InputEventsLastArrivalTime** is updated with every received event's enqueued time 

_2) Is time moving forward? If actual events are read, punctuation might not be issued._ 

**InputEventsLastPunctuationTime** indicates when a punctuation was issued to keep time moving forward. Data flow can get blocked if punctuation is not issued. 

_3) Are there any errors in the input?_ 

**InputEventsEventDataNullTotal** holds a count of events with null data <br>
**InputEventsSerializerErrorsTotal** holds a count of events that could not be deserialized correctly <br>
**InputEventsDegradedTotal** holds a count of events that had an issue other than deserialization problems

_4) Are events getting dropped/adjusted?_ 

**InputEventsEarlyTotal** provides the number of events with an application timestamp before the high watermark. <br>
**InputEventsLateTotal** provides the number of events with an application timestamp after the high watermark. <br>
**InputEventsDroppedBeforeApplicationStartTimeTotal** provides the number events dropped before the job start time. 

_5) Are we following behind in reading data?_ 

**InputEventsSourcesBackloggedTotal** tells us how many more messages need to be read for EventHub and IoTHub inputs. 

_To open a Microsoft Support case_

If you are still not able to figure out what is going on, then go to operations log, select one of the latest entries and click Details button at the bottom of the screen and copy all the details on that page and use that info to supply to Microsoft Support. 

Additionally, if possible, include sample data from a time when the job was expected to produce output.  

