<properties
	pageTitle="extensionsnapshotfailedcom"
	description="extensionsnapshotfailedcom"
	infoBubbleText="VM Snapshot operation failed due to COM+ error. See details on the right."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
	articleId="azurebackup-crc-extensionsnapshotfailedcom"
	diagnosticScenario="azurebackup-crc-extensionsnapshotfailedcom"
	selfHelpType="diagnostics"
	supportTopicIds="32553276"
	productPesIds="15207"
	cloudEnvironments="public"
/>

# ExtensionSnapshotFailedCOM
<!--issueDescription-->
Snapshot operation failed due to COM+ error.
<!--/issueDescription-->

## **Recommended Steps**
We have investigated and detected there could be an issue from Windows service **COM+ System Application** which may prevent your backup installation/operation.
To resolve this issue we recommend you to try the below steps. <br>

**Cause 1**: **Error due to COM+ System Application**

* Try starting/restarting Windows service **COM+ System Application** (from an elevated command prompt **- net start COMSysApp**).
* Ensure Distributed Transaction Coordinator is running as **Network Service**. If not, change it to run as Network Service & restart **COM+ System Application**.
* If unable to restart the service, then uninstall/install service **Distributed Transaction Coordinator** by following below steps:

	* Stop the MSDTC service
	* Open a command prompt (cmd)
	* Run command **msdtc -uninstall**
	* Run command **msdtc -install**
	* Start the MSDTC service
	* After completing above troubleshooting steps, trigger an ad-hoc backup from [portal.azure.com](https://portal.azure.com) to see if the backup operation succeeds.<br>

**Cause 2**: **Error due to IaaS VM provider Service<br>**
If iaasvm provider service is not installed properly then you might encounter this issue. To resolve this issue set the following 2 Reg-Keys as false and trigger a backup.

* **HKEY_LOCAL_MACHINE -> SOFTWARE -> Microsoft -> BCDRAgent -> IsProviderInstalled**
* **HKEY_LOCAL_MACHINE -> SOFTWARE -> Microsoft -> BCDRAgentPersistentKeys -> IsCommonProviderInstalled**
