<properties
	pageTitle="ExtensionInstallationFailedCOM"
	description="ExtensionInstallationFailedCOM"
	service="microsoft.recoveryservices"
	infoBubbleText="Snapshot operation failed due to VSS Writers in bad state"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-extensioninstallationfailedcom"
	diagnosticScenario="azurebackup-crc-extensioninstallationfailedcom"
	selfHelpType="diagnostics"
	supportTopicIds="32553276,32553277"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
/>

# ExtensionInstallationFailedCOM

<!--issueDescription-->
## **Extension installation/operation failed due to a COM+ error**
<!--/issueDescription-->

## **Recommended Steps**
We identified that your backup operation was failing due to an issue from Windows service COM+ System Application. To resolve this issue we recommend you to try the following steps:

* Try starting/restarting Windows service **COM+ System Application** (from an elevated command prompt **- net start COMSysApp**).
* Ensure **Distributed Transaction Coordinator** services is running as **Network Service** account. If not, change it to run as **Network Service** account and restart **COM+ System Application**.
* If unable to restart the service, then reinstall **Distributed Transaction Coordinator** service by following the below steps:
	* Stop the MSDTC service
	* Open a command prompt (cmd)
	* Run command **msdtc -uninstall**
	* Run command **msdtc -install**
	* Start the MSDTC service
