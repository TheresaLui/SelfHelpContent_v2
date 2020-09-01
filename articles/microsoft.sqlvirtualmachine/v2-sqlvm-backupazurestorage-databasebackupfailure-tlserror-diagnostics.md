<properties
	pageTitle="Database Backup Failure with TLS Error"
	description="Database Backup Failure with TLS Error"
	infoBubbleText="Database Backup Failure with TLS Error"
	service="Microsoft.SqlVirtualMachine"
	resource="SqlVirtualMachines"
	ms.author="ujpat"	
	authors="ujpat"
	displayOrder="1"
	selfHelpType="diagnostics"
	supportTopicIds="32740094"
	resourceTags="windowsSQL"
	productPesIds="14745,16342"
	cloudEnvironments="public,fairfax, usnat, ussec, blackforest, mooncake"
	articleId="cdbdbfc9-20b1-48c9-bfc9-ddd7c45b0fe2-azurestorage"
	ownershipId="AzureData_AzureSQLVM"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
This issue can occur on SQL 2012,2014 and 2016 versions where .Net version does not have TLS Preference as TLS 1.2.
<!--/issueDescription-->

## **Recommended Steps**

- Backup to Microsoft Azure blob storage service URL isn’t compatible for TLS 1.2, and can be fixed by following this [KB article](https://support.microsoft.com/help/4017023/fix-sql-server-2014-or-2016-backup-to-microsoft-azure-blob-storage-ser)

## **Recommended Documents**

* [FIX: SQL Server 2014 or 2016 Backup to Microsoft Azure Blob storage service URL isn't compatible for TLS 1.2](https://support.microsoft.com/en-in/help/4017023/fix-sql-server-2014-or-2016-backup-to-microsoft-azure-blob-storage-ser)
