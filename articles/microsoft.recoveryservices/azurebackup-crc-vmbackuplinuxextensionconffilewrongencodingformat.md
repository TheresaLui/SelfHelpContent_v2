<properties
	pageTitle="VMBackupLinuxExtensionConfFileWrongEncodingFormat"
	description="VMBackupLinuxExtensionConfFileWrongEncodingFormat"
	infoBubbleText="Linux backup operation might have failed, because there is a change in Linux VM Backup Extension Configuration file"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-vmbackuplinuxextensionconffilewrongencodingformat"
	diagnosticScenario="azurebackup-crc-vmbackuplinuxextensionconffilewrongencodingformat"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error VMBackupLinuxExtensionConfFileWrongEncodingFormat

<!--issueDescription-->
We have identified that your Linux backup operation may have failed because there is a change in the Linux VM Backup Extension Configuration file.
<!--/issueDescription-->

## **Recommended Steps**

To resolve this issue:

- The configuration values in Linux VM Backup Extension Config file might be modified. We recommend changing the encoding format of the Linux VM *Backup Extension Conf file (/etc/azure/vmbackup.conf)* to ASCII by using a text editor or by using the following command: `iconv -t ASCII /etc/azure/vmbackup.conf`
