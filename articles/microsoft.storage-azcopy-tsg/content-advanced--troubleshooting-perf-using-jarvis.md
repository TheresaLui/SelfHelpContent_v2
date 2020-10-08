<properties
	pageTitle="Advanced: Troubleshooting Perf Using Jarvis"
	description="Advanced: Troubleshooting Perf Using Jarvis"
        service="Microsoft.Storage"
        resource="Microsoft.Storage/storageAccounts"
	authors="rimayber"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="bb5277dc-1349-45d5-8c0b-e7ca6ed16c1c"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Advanced: Troubleshooting Perf Using Jarvis

If a customer reports slow upload/download speed using AzCopy, you can use Jarvis Logs as well as **ASC->Xdiagnostics** to troubleshoot performance issues.

1. Search the Jarvis logs by specifying **StorageAccount, TenantName** in the **XStore Namespace and FrontEndSummaryPerfLogs, NativeFePerfMetric event tables**.
2. Once the log search is completed, aggregate the logs by **Storage Account, Operation, Status, InternalStatus**.
    1. *Sample request: {"PreciseTimeStamp":"2019-06-12T14:54:50.0105297Z","RoleInstance":"MS-SYD23PrdStr01A:Nephos.Blob_IN_10","ActivityId":"6e587bc7-001e-000a-4b2e-217267000000","RequestHeaderSize":"609","RequestSize":"886660","TimeInMs":"138344","ProcessingTimeInMs":"10","MaxAllowedTimeoutInMs":"2460000","SlaUsedInMs":"250","ReadLatencyInMs":"138333","WriteLatencyInMs":"1","ClientIP":"203.43.179.114:41574","RequestUrl":"https://hillsveeamoffsite.blob.core.windows.net:443/hillsveeamoffsite/Backups/sydorabk02p_ORA_T1%20-%20sydorabk02p/sydorabk02p_ORA_T1%20-%20sydorabk02p_D79CD2019-06-04T010838.vib?comp=block&blockid=bEZBZEF0M014UTdMemZjQUxqMVgwdz09MTIzNDU2NzgtMDAwMzU4&timeout=300","ClientRequestId":"412bb33b-dd89-41c4-8890-889fe69633c7","TotalFeTimeInMs":"7","TotalTableServerTimeInMs":"0","TotalTableServerRoundTripCount":"0","LastTableServerInstanceName":"","LastTableServerErrorCode":"None","PartitionKey":"Backups/sydorabk02p_ORA_T1 - sydorabk02p/sydorabk02p_ORA_T1 - sydorabk02p_D79CD2019-06-04T010838.vib","AccountConcurrentReq":"5","OverallConcurrentReq":"32","LastTSPartition":"","TotalAuthTimeInMs":"0.122","AuthenticationTimeInMs":"0.116","AuthorizationTimeInMs":"0.006","TotalDecompressionTimeInMs":"-138333","Tid":"81700","Pid":"52164"}*

## Analyze a failed request and look for following values

1. TimeInMs (or E2E Latency) = ProcessingTimeInMs + ReadLatencyInMs + * WriteLatencyInMs
   * ProcessingTimeInMs
   * WriteLatencyInMs
   * ReadLatencyInMs
   * TotalFeTimeInMs
   * TotalTableServerTimeInMs
2. If Operation==**GetBlob/GetBlobOperties** etc. and the MAX time out of TimeInMs is spent at WriteLatencyInMs that indicates Storage Service is unable to write to the client causing NetworkError. Look for **UserAgent and ClientIP** Address to narrow down the Client Information.
3. If Operation==**PutBlob/PutBlockProperties /PutBloc** etc. and the MAX time out of TimeInMs is spent at ReadLatencyInMs that indicates Storage Service is unable to Read from the client causing NetworkError. Look for **UserAgent and ClientIP** Address to narrow down the Client Information.
4. If the MAX Time Spent is during **TotalFeTimeInMs / TotalTableServerTimeInMs** use **XDiagnostics** to root cause the issue.
   1. From Azure Storage Center, Select the Storage Account -> XDiagnostics
   2. Click on CREATE REPORT, Enter the Start / End Time Frame, and run the Report. 
   3. After report generation is completed. View Sample request by clicking on **EYEICON** which contains NetworkError.
   4. After sample request is expanded click on **CREATE REPORT** and run the report with PrePopulated Activity ID. And it will search for XDS logs and display the root cause statement. 
