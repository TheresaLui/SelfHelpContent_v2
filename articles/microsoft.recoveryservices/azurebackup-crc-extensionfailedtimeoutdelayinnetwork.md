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

To resolve the ExtensionFailedTimeoutDelayInNetwork issue, perform the below:

* Ensure there is no network delay that might lead to communication latencies
* If you have configured a proxy server, ensure that it is not introducing network delays. System Account Proxy settings can be checked on Internet Explorer opened under system account, using [these steps](https://docs.microsoft.com/azure/backup/backup-azure-arm-vms-prepare#set-up-the-proxy)
* If no proxy is intended to be configured, then enforce localhost to be treated as proxy by adding an entry in hosts file as given below
	* Add 127.0.0.1 wpad to the C:\Windows\System32\drivers\etc\host file, if this entry does not help then retry by adding 127.0.0.1 wpad wpad.FQDN to the file
	* Run the command ipconfig/flushdns
* Set reg-keys to enforce snapshots to be taken through Host, run the below command from elevated (as admin) command-prompt. This will not use VM Network stack for snapshots and retry the backup operation.

` REG ADD "HKLM\SOFTWARE\Microsoft\BcdrAgentPersistentKeys" /v SnapshotMethod /t REG_SZ /d firstHostThenGuest /f `
