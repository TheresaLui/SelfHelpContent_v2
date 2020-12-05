<properties
      pageTitle="SalFileProviderUnInitializationFailed"
      description="SalFileProviderUnInitializationFailed"
      infoBubbleText="We have identified that you encounter this error during the backup operation"
      service="microsoft.recoveryservices"
      resource="backup"
      authors="srinathv"
      ms.author="srinathv"
      articleId="azurebackup-crc-salfileproviderunInitializationfailed"
      diagnosticScenario="azurebackup-crc-salfileproviderunInitializationfailed"
      selfHelpType="diagnostics"
      supportTopicIds="32553277"
      productPesIds="15207"
      cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# SalFileProviderUnInitializationFailed

<!--issueDescription-->
We have identified that you encountered this error during the backup operation.
<!--/issueDescription-->

The causes and steps to mitigate the issues are listed below:<br>

**Step 1**: Follow the steps listed in this [article](https://docs.microsoft.com/azure/backup/backup-azure-manage-mars#add-exclusion-rules-to-existing-policy) to exclude the following folders:
- **Exclude the Scratch folder** located at *C:\Program Files\Microsoft Azure Recovery Services Agent\Scratch* from the Scheduled Backup. <br>
- **Exclude the MARS Agent Bin folder** located at *C:\Program Files\Microsoft Azure Recovery Services Agent\bin* from the Scheduled Backup.<br>

**Step 2**: Change ownership to **System** for all the VHD folders in the scratch folder by following the below steps:<br>
- Navigate to Scratch folder location, default path is C:\Program Files\Microsoft Azure Recovery Services Agent\Scratch.
- Right-click on any VHD folder and select **Security** tab. Click **Advance** and **Change** Owners.<br>
    Type **SYSTEM** and click **Search** button.<br>
    Select **SYSTEM** from the list and click **OK**.<br>
- Reboot the server.<br>

**Step 3**: Retry backup operation.
