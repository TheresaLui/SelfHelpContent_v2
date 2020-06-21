<properties
	          pageTitle="usererrorunsupporteddisksize"
	          description="usererrorunsupporteddisksize"
		  infoBubbleText="Backup operation was failing due to the disk size limit. See details on the right."
	          service="microsoft.recoveryservices"
	          resource="backup"
	          authors="srinathv"
	          ms.author="srinathv"
		  articleId="azurebackup-crc-usererrorunsupporteddisksize"
	          diagnosticScenario="azurebackup-crc-usererrorunsupporteddisksize"
	          selfHelpType="diagnostics"
	          supportTopicIds="32553276"
	          productPesIds="15207"
	          cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>


# Error UserErrorUnsupportedDiskSize

<!--issueDescription-->
We have identified that your backup operation failed because Azure Backup does not currently support disk sizes greater than 4095GB. 
<!--/issueDescription-->

## **Recommended Steps**

* For more information on supported configurations refer this [article](https://docs.microsoft.com/azure/backup/backup-support-matrix-iaas)
* Review the [benefits](https://aka.ms/AB-IR-feature-considerations), including the ability to backup disks up to 4TB
* Make sure you read the [considerations](https://aka.ms/AB-IR-feature-considerations) section
* Complete the upgrade following these [instructions](https://aka.ms/AB-IR-upgrade)
