<properties
	pageTitle="extensionfailedtimeoutdelayinnetwork"
	description="extensionfailedtimeoutdelayinnetwork"
	infoBubbleText="Snapshot operation failed due to delay in network calls made to take disk blob-snapshots."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
	ms.author="srinathv"
	articleId="azurebackup-crc-extensionfailedtimeoutdelayinnetwork"
	diagnosticScenario="azurebackup-crc-extensionfailedtimeoutdelayinnetwork"
	selfHelpType="diagnostics"
	supportTopicIds=""
	productPesIds="15207"
	cloudEnvironments="public"
/>

# Error ExtensionFailedTimeoutDelayInNetwork

<!--issueDescription-->
We have identified that your backup operation failed due to the proxy-server that has introduced the network delay.
<!--/issueDescription-->

## **Recommended Steps**
To resolve ExtensionFailedTimeoutDelayInNetwork ensure there are no network delays or delays due to proxy-server.<br/>
Follow these steps to resolve the issue:<br/> 

* Ensure there is no network delay that might lead to communication latencies. <br/>
* Use bitsadmin Util to set No-Proxy to be used for LocalSystem account using the below command:<br/>
	`
  bitsadmin /Util /SetIEProxy LOCALSYSTEM NO_PROXY
  `

## **Recommended Document**
For more information on bitsadmin util, refer this [document](https://docs.microsoft.com/windows-server/administration/windows-commands/bitsadmin-util-and-setieproxy)
