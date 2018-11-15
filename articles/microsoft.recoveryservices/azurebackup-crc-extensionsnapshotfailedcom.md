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
Snapshot operation failed due to COM+ error or due to an issue with the IaaS VM provider Service.
<!--/issueDescription-->

## **Recommended Steps**
We have investigated and detected there could be an issue from Windows service **COM+ System Application** which may prevent your backup installation/operation.
There are two common causes for this issue. Follow the steps outlined in the **Error due to COM+ System Application** section. If your backup continues to fail, then follow the steps in the **Error due to IaaS VM provider Service** section.
<br>

**Error due to COM+ System Application**

* Login to the impacted VM and try starting/restarting Windows service **COM+ System Application** (from an elevated command prompt **- net start COMSysApp**).
* Open VM services using services.msc and ensure the **Distributed Transaction Coordinator** service is running in the VM services as **Network Service**, if not, change it to run as **Network Service** and then restart the **COM+ System Application** service.
* If unable to restart the service, then uninstall/install service **Distributed Transaction Coordinator** service by following below steps:

	* Stop the MSDTC service
	* Open a command prompt (cmd)
	* Run command **msdtc -uninstall**
	* Run command **msdtc -install**
	* Start the MSDTC service
	* After completing above troubleshooting steps, trigger an ad-hoc backup from [portal.azure.com](https://portal.azure.com) to see if the backup operation succeeds.<br>

**Error due to IaaS VM provider Service<br>**

* Login to the impacted VM and open the **Registry Editor** by typing **regedit** in the **Run** window
* Set the following 2 Reg-Keys to false <br>

	- **HKEY_LOCAL_MACHINE -> SOFTWARE -> Microsoft -> BCDRAgent -> IsProviderInstalled** <br>
	
	- **HKEY_LOCAL_MACHINE -> SOFTWARE -> Microsoft -> BCDRAgentPersistentKeys -> IsCommonProviderInstalled** <br>
	
* Trigger the backup operation from Azure Portal
