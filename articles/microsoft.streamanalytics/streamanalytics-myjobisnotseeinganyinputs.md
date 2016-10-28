<properties 
	pageTitle="My job is not seeing any inputs"
	description="My job is not seeing any inputs"
	service="microsoft.streamanalytics"
	resource="streamingjobs"
	authors="kschaefer13"
	displayOrder="2"
	selfHelpType="resource"
	supportTopicIds=""
	productPesIds=""
	cloudEnvironments="public"
/>

# My job is not seeing any inputs

## **Recommended steps**
1. Verify connectivity to inputs and outputs by using the "Test Connection" button for each of the inputs. If this fails, verify the credentials for input sources or output sinks. 
2. Use "Service Bus Explorer" to connect to Azure EventHub (if EventHub input is used) to verify that input data is flowing into EventHub. 
3. Use the "Sample Data" button for each of the inputs and download the input sample data. 
    * Verify CSV includes headers for every event or batch of events. 
    * Verify CSV headers don’t contain spaces if output is SQL. 
4. Inspect the sample data to understand the shape of the data: the schema, and the data types. 
5. On the Query tab, use the "Test" button to test the query and use the sample data downloaded to test the query. Examine any errors and attempt to remediate them.  
6. Type in the query, start the Job and check if the job works as desired with low load. 
7. Once the job status changes to "Running", depending on the duration stipulated in the query, the output can be seen in the Sink data-source. 
8. If no output is obtained after the expected duration (based on the query), try the following: 
    * Look at Monitoring Metrics on Monitor tab. The metrics here are delayed by about couple of minutes as they are aggregated values over last minute. 
    * Look at the metrics for Input Events, Runtime Errors, Data Conversion Errors. 
        * If Input Events > 0, the ASA job is able to read data. If not, then the problems may be 
            * If Timestamp By is used, make sure the events have timestamps greater than the start time. 
            * Look at the data source and see if it has valid data for this job using Service Bus Explorer (if Event Hub is used as input) 
            * Check if the Data serialization format and Encoding are as expected. 
            * If using Event Hub, the Body of the Message may be Null. 

If there are no issues, the data flow will need to be analyzed. Analyzing the data flow systematically can be done with the job diagram that shows a visual representation of the job by clicking on the "Job diagram" button in the "Settings" blade of the of the Stream Analytics job. For existing jobs, it is necessary to restart the job first. 

Learn about the job diagram [here.](https://aka.ms/job_diagram)

In the job diagram, examine the following input metrics to help answer the following targeted questions about jobs getting data from its input sources. If the query is partitioned, examine each partition.  

_1) How much data is actually being read?_ 

**InputEventsSourcesTotal** metric provides the number of data units read, e.g. number of blobs. <br>
**InputEventsTota**l provides the number of events read. This metric is available per partition. <br>
**InputEventsInBytesTotal** provides the number of bytes read. <br>
**InputEventsLastArrivalTime** is updated with every received event's enqueued time 

_2) Is time moving forward? If actual events are read, punctuation might not be issued._ 

**InputEventsLastPunctuationTime** indicates when a punctuation was issued to keep time moving forward. Data flow can get blocked if punctuation is not issued. <br>

_3) Are there any errors in the input?_ 

**InputEventsEventDataNullTotal** holds a count of events with null data <br>
**InputEventsSerializerErrorsTotal** holds a count of events that could not be deserialized correctly <br>
**InputEventsDegradedTotal** holds a count of events that had an issue other than deserialization problems 

_4) Are events getting dropped/adjusted?_ 

**InputEventsEarlyTotal** provides the number of events with an application timestamp before the high watermark. <br>
**InputEventsLateTotal** provides the number of events with an application timestamp after the high watermark. <br>
**InputEventsDroppedBeforeApplicationStartTimeTotal** provides the number events dropped before the job start time 

_5) Are we following behind in reading data?_ 

**InputEventsSourcesBackloggedTotal** tells us how many more messages need to be read for EventHub and IoTHub inputs. 
