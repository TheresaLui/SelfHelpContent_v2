<properties
      pageTitle="SalFileProviderUnInitializationFailed"
      description="SalFileProviderUnInitializationFailed"
      infoBubbleText="We have identified that you encounter this error during the backup operation"
      service="microsoft.recoveryservices"
      resource="backup"
      authors="srinathv"
      ms.author="srinathv"
      articleId="azurebackup-crc-salfileprovideruninitializationfailed"
      diagnosticScenario="azurebackup-crc-salfileprovideruninitializationfailed"
      selfHelpType="diagnostics"
      supportTopicIds=""
      productPesIds="15207"
      cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# SalFileProviderUnInitializationFailed

<!--issueDescription-->
We have identified that you encountered this error during the backup operation.
<!--/issueDescription-->

Use these steps to mitigate the issue as follows.<br>

## **Recommended Steps**

Step 1: Follow the steps listed in this [article](https://docs.microsoft.com/azure/backup/backup-azure-manage-mars#add-exclusion-rules-to-existing-policy) to exclude the following folders:
* Exclude the Scratch folder from the Scheduled Backup. This folder is located at C:\Program Files\Microsoft Azure Recovery Services Agent\Scratch<br>
* Exclude the MARS Agent Bin folder from the Scheduled Backup. This folder is located at C:\Program Files\Microsoft Azure Recovery Services Agent\bin <br>

Step 2: Change ownership to **System** for all of the VHD folders in the scratch folder by following the below steps:<br>
* Navigate to Scratch folder location, default path is C:\Program Files\Microsoft Azure Recovery Services Agent\Scratch.
* Right-click any VHD folder and select the **Security** tab. Select **Advance** and **Change** Owners.<br>
    * Type **SYSTEM** and select the **Search** button.<br>
    * Select **SYSTEM** from the list and click **OK**.<br>
* Restart the server.<br>

Step 3: Retry the backup operation
