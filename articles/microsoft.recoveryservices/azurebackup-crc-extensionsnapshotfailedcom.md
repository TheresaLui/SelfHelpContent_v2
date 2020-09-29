<properties
	pageTitle="extensionsnapshotfailedcom"
	description="extensionsnapshotfailedcom"
	infoBubbleText="VM Snapshot operation failed due to COM+ error. See details on the right."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
	ms.author="srinathv"
	articleId="azurebackup-crc-extensionsnapshotfailedcom"
	diagnosticScenario="azurebackup-crc-extensionsnapshotfailedcom"
	selfHelpType="diagnostics"
	supportTopicIds="32553276"
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# ExtensionSnapshotFailedCOM
<!--issueDescription-->
We have identified a problem that is preventing the successful installation or operation of your backup. This problem can be caused by an issue in either a Windows service called **COM+ System Application** or in the **IaaS VM provider service**. 
<!--/issueDescription-->

## **Recommended Steps**
To resolve this issue, first complete the steps outlined in the section **Error due to COM+ System Application**. If you continue to experience issues with your backup, then complete the steps in the section **Error due to IaaS VM provider service**. <br>

**Error due to COM+ System Application**

* In the **Run** window, enter `services.msc` and press enter
* Double click on the service called **Distributed Transaction Coordinator**. Go to the **Log on** tab and verify that the service is running as **Network Service**. If this is not the case, then:

	* Click **Browse** to open the **Select User** dialog
	* Enter **Network Service** and click **Check Names**. The name of the account will be underlined.
	* Click **OK** to get back to the service dialog
	* Click on the **General** tab and restart the service and click **OK**
	* Back in the Services window, right click on the **COM+ System Application service** and select **Restart**
	
* If you are unable to restart the **COM+ System Application service**, then uninstall/install Distributed Transaction Coordinator service with these steps:

	* Stop the MSDTC service
	* Open a command prompt (cmd)
	* Run command `msdtc -uninstall`
	* Run command `msdtc -install`
	* Start the MSDTC service
	
* After completing above troubleshooting steps, trigger an ad-hoc backup from the [portal.azure.com](https://portal.azure.com) to see if the backup operation succeeds. **If the operation fails, then complete the steps in the following section.**
	
**Error due to IaaS VM provider Service**

* Login to the impacted VM and open the **Registry Editor** by typing `regedit` in the **Run** window
* Set the following 2 Reg-Keys to false <br>

	- **HKEY_LOCAL_MACHINE -> SOFTWARE -> Microsoft -> BCDRAgent -> IsProviderInstalled** <br>
	
	- **HKEY_LOCAL_MACHINE -> SOFTWARE -> Microsoft -> BCDRAgentPersistentKeys -> IsCommonProviderInstalled** <br>
		
* Trigger the backup operation from the [Azure Portal](https://portal.azure.com)
