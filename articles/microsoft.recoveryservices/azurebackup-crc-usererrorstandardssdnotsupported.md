<properties
	pageTitle="usererrorstandardssdnotsupported"
	description="usererrorstandardssdnotsupported"
	infoBubbleText="Currently Azure Backup does not support Standard SSD disks. See details on the right."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-usererrorstandardssdnotsupported"
	diagnosticScenario="azurebackup-crc-usererrorstandardssdnotsupported"
	selfHelpType="diagnostics"
	supportTopicIds="32553276,32553277,32553285"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
/>

# UserErrorStandardSSDNotSupported

<!--issueDescription-->
We found that you are using Standrd SSD disk for this **<!--$DatasouceName-->DatasouceName<!--/$DatasouceName-->** VM. However, Azure Backup currently supports Standard SSD disks only for vaults that are upgraded to [Instant Restore](https://aka.ms/AB-instant-Restore). 
<!--/issueDescription-->

## **Recommended Steps**

To verify and upgrade this **<!--$VaultName-->VaultName<!--/$VaultName-->** vault to Instant Restore, see this [article](https://aka.ms/AB-instant-Restore). Make sure you read the [considerations](https://aka.ms/AB-IR-feature-considerations) section.

## **Recommended Documents**

Review the [benefits](https://aka.ms/AB-IR-feature-considerations), including the ability to backup disks up to 4TB
