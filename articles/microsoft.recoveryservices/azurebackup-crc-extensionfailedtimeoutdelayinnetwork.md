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
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error ExtensionFailedTimeoutDelayInNetwork

<!--issueDescription-->
We have identified that your backup operation failed due to the proxy server introducing a network delay.
<!--/issueDescription-->

## **Recommended Steps**

* Ensure there are no network delays or delays due to proxy server
* Ensure there is no network delay that might lead to communication latencies
* Use bitsadmin Util to set No-Proxy to be used for LocalSystem account: `bitsadmin /Util /SetIEProxy LOCALSYSTEM NO_PROXY`

## **Recommended Documents**

* [Bitsadmin Utility](https://docs.microsoft.com/windows-server/administration/windows-commands/bitsadmin-util-and-setieproxy)
