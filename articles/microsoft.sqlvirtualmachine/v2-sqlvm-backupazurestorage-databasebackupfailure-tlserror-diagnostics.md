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
This issue can occur due to .Net version installed on your machine.
<!--/issueDescription-->

## **Recommended Steps**
- This error occurs if your client server enabled Transport Layer Security (TLS) protocol version 1.2 with the following registry.

	```
	HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Control\SecurityProviders\SCHANNEL\Protocols\TLS 1.2\Client
	Value:0
	Name: Enabled
	Type: REG_DWORD
	Data: 0x1
	```

- To fix this issue install the below:
	- [Cumulative Update 7 for SQL Server 2016 RTM](https://support.microsoft.com/en-in/help/4024304)
	- [Cumulative Update 4 for SQL Server 2016 SP1](https://support.microsoft.com/en-in/help/4024305)
	- [Cumulative Update 5 for SQL Server 2014 SP2](https://support.microsoft.com/en-in/help/4013098)

## **Recommended Documents**

* [FIX: SQL Server 2014 or 2016 Backup to Microsoft Azure Blob storage service URL isn't compatible for TLS 1.2](https://support.microsoft.com/en-in/help/4017023/fix-sql-server-2014-or-2016-backup-to-microsoft-azure-blob-storage-ser)


