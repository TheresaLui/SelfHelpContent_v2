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
    cloudEnvironments="public, MoonCake, fairfax, usnat, ussec"
	articleId="84b0f3f7-44eb-4194-8bf5-9d008b8aee0b"
	ownershipId="AzureData_StreamAnalytics"
/>

# My job is not outputting data

## **Recommended steps**
1. Verify connectivity to inputs and outputs by using the "Test Connection" button for each of the inputs and outputs. 
2. Use "Service Bus Explorer" to connect to Azure EventHub (if EventHub input is used) to verify that input data is flowing into EventHub. 
3. Use the “Sample Data” button for each of the inputs and download the input sample data. 
4. Inspect the sample data to understand the shape of the data: the schema, and the data types. 
5. On the Query tab, use the “Test” button to test the query and use the sample data downloaded to test the query. Examine any errors and attempt to remediate them.  
6. If Timestamp By is used, make sure the events have timestamps greater than the job start time. 
7. Re-build the query progressively from simple select statement to more complex aggregates using steps. Using WITH clause to build up the query logic, step by step.
8. Watch out for common gotachas where it is possible that your query is functioning just fine but: <br>
  * A where clause in the query filtered out their events that prevented outputs from being generated. <br>
  * The window size is large enough that you’ll need to wait for the corresponding duration to see an output from the query. <br>
  * Timestamp for events is before the job start time and therefore events are being dropped. <br>
9. If all these steps worked fine, go to Settings blade and pick event ordering. Make sure this policy configuration makes sense for your job. It should be noted that this policy is not applied when the “Test” button is used to test the query. This is a difference between testing in browser versus running the job for real. 
10. Start the Job and check if the job works as desired.  
11. Once the job status changes to "Running", depending on the duration stipulated in the query, the output can be seen in the Sink data-source. 
12. If no output is obtained after the expected duration (based on the query), try the following: <br>
    * Look at Monitoring Metrics on Monitor tab. The metrics here are delayed by about couple of minutes as they are aggregated values over last minute. <br>
    * Look at the metrics for Input Events, Runtime Errors, Data Conversion Errors. <br>
        * If Input Events > 0, the ASA job is able to read data. If not, then the problems may be <br>
            * Look at the data source and see if it has valid data for this job using Service Bus Explorer (if Event Hub is used as input) <br>
            * Check if the Data serialization format and Encoding are as expected. <br>
            * If using Event Hub, the Body of the Message may be Null. <br>
        * If Data Conversion Errors > 0 and climbing, that means: <br>
            * Job may not be able to deserialize the events. <br>
            * Events schema may not match the defined/expected schema of the events in the query. <br>
            * DataType of some of the fields in the Event may not be what is expected. <br>
        * If Runtime Errors > 0, means that the ASA Job is able to receive the data but is getting errors while processing the query. Go to the Operation Logsand filter on "Failed" status to find all these errors. <br>
        * If InputEvents > 0 and OutputEvents = 0, means one of the following: <br>
            * Query processing resulted in zero output events. <br>
            * Events or its fields may be malformed, so resulted in zero output after query processing. <br>
            * Unable to push data to the output sink for connectivity/authentication reasons. <br>
            * In all of these error cases, operations log messages explain additional details (including what is happening), except for the cases the query logic filtered out all events. If the processing of multiple events generates errors, Stream Analytics logs the first 3 error messages of the same type within 10 minutes to Operations logs and then suppress additional identical errors with a message that reads "Errors are happening too rapidly, these are being suppressed". <br>

When outputs going to a specific output type are not seen, redirect the output to different output type that is less complex (such as Azure Blobs) and check if the output can be seen up there (using Storage Explorer). 

_To open a Microsoft Support case_

If you are still not able to figure out what is going on, then go to operations log, select one of the latest entries and click Details button at the bottom of the screen and copy all the details on that page and use that info to supply to Microsoft Support. 

Additionally, if possible, include sample data from a time when the job was expected to produce output.
