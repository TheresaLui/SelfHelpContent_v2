<properties
	pageTitle="Database Backup failure due to proxy server issues"
	description="Database Backup failure due to proxy server issues"
	infoBubbleText="Database Backup failure due to proxy server issues"
	service="Microsoft.SqlVirtualMachine"
	resource="SqlVirtualMachines"
	ms.author="ujpat"	
	authors="ujpat"
	displayOrder="1"
	diagnosticScenario=""
	selfHelpType="diagnostics"
	supportTopicIds="32740094"
	resourceTags="windowsSQL"
	productPesIds="14745,16342"
	cloudEnvironments="public,fairfax, usnat, ussec, blackforest, mooncake"
	articleId="9900c3c4-acab-4349-99eb-018ef9122f3f-azurestorage"
	ownershipId="AzureData_AzureSQLVM"
/>
# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
The error indicates backups might have failed due to proxy authentication errors or due to connection throttling.
<!--/issueDescription-->

## **Recommended Steps**
 
  - Connection throttling by Proxy Servers  
  	- Proxy Servers can have settings that limit the number of connections per minute. The Backup to URL process is a multi-threaded process and hence can go over this limit. If this happens, the proxy server kills the connection. To resolve this issue, change the proxy settings so SQL Server is not using the proxy
  - Sometimes the default settings are not picked up causing proxy authentication errors. To resolve this issue, create a configuration file that allows the Backup to URL process to use the default proxy settings using the following steps:
  	- Create a configuration file namedBackuptoURL.exe.config, with the following xml content:
		```xml		
		\<configuration\>Sample      
        \</configuration\> 
		```
	
     
	- Place the configuration file in the Binn folder of the SQL Server Instance. For example, if my SQL Server is installed on the C drive of the machine, place the configuration file in C:\Program Files\Microsoft SQL Server\MSSQL13.\<InstanceName>\MSSQL\Binn.

## **Recommended Documents**

* [Proxy settings & backup to URL (Azure blob storage)](https://blogs.msdn.microsoft.com/psssql/2016/09/29/proxy-settings-backup-to-url-azure-blob-storage/)
* [SQL Server backup to URL best practices and troubleshooting: Proxy Errors](https://docs.microsoft.com/sql/relational-databases/backup-restore/sql-server-backup-to-url-best-practices-and-troubleshooting?view=sql-server-ver15#proxy-errors)