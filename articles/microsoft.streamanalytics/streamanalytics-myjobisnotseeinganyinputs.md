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
	cloudEnvironments="public, MoonCake, fairfax, usnat, ussec"
	articleId="50ac01a9-1177-4567-9c63-892ed4c69faf"
	ownershipId="AzureData_StreamAnalytics"
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
        * If Input Events > 0, the ASA job is able to read data. If not, problems may be the following:
            * If Timestamp By is used, make sure the events have timestamps greater than the start time. 
            * Look at the data source and see if it has valid data for this job using Service Bus Explorer (if Event Hub is used as input) 
            * Check if the Data serialization format and Encoding are as expected. 
            * If using Event Hub, the Body of the Message may be Null. 

