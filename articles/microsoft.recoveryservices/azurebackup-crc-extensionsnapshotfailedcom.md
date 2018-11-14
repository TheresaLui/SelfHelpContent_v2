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
Snapshot operation failed due to COM+ error or due to issue with the IaaS VM provider Service.
<!--/issueDescription-->

## **Recommended Steps**
We have investigated and detected there could be an issue from Windows service **COM+ System Application** which may prevent your backup installation/operation.
There are two common causes for this issue. Follow the steps outlined in the **Error due to COM+ System Application** section. If your backup continues to fail, then follow the steps in the **Error due to IaaS VM provider Service** section.
<br>

**Error due to COM+ System Application**

* Login to the impacted VM and try starting/restarting Windows service **COM+ System Application** (from an elevated command prompt **- net start COMSysApp**).
* Ensure the **Distributed Transaction Coordinator** service is running in the VM services (services.msc) as **Network Service**, if not, change it to run as **Network Service** and then restart the **COM+ System Application** service.
* If unable to restart the service, then uninstall/install service **Distributed Transaction Coordinator** service by following below steps:

	* Stop the MSDTC service
	* Open a command prompt (cmd)
	* Run command **msdtc -uninstall**
	* Run command **msdtc -install**
	* Start the MSDTC service
	* After completing above troubleshooting steps, trigger an ad-hoc backup from [portal.azure.com](https://portal.azure.com) to see if the backup operation succeeds.<br>

**Error due to IaaS VM provider Service<br>**
If iaasvm provider service is not installed properly then you might encounter this issue. To resolve this issue, login to the impacted VM and set the following 2 Reg-Keys in the **Registry Editor** as false and then trigger a backup operation.

* **HKEY_LOCAL_MACHINE -> SOFTWARE -> Microsoft -> BCDRAgent -> IsProviderInstalled**
* **HKEY_LOCAL_MACHINE -> SOFTWARE -> Microsoft -> BCDRAgentPersistentKeys -> IsCommonProviderInstalled**
