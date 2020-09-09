<properties
  pagetitle="Synapse Studio, Azure Portal and Client Tools/Synapse Studio"
  service="microsoft.synapse"
  resource="workspaces"
  ms.author="saltug,goventur"
  selfhelptype="Generic"
  supporttopicids="32738836"
  resourcetags=""
  productpesids="15818"
  cloudenvironments="public,fairfax,blackforest,mooncake,usnat,ussec"
  articleid="synapse-synapsestudioazureportalandclienttools-synapsestudio"
  ownershipid="AzureData_SQLDataWarehouse" />
# Synapse Studio, Azure Portal and Client Tools/Synapse Studio

### Known issues

* If you have multiple AAD logins that is cached to your browser, opening Synapse Studio from Portal might not complete as your browser might try to use a different AAD account to authenticate you to Synapse Studio system. You might need to log off (or remove) other AAD account that is cached to your browser to complete your login to Synapse Studio.
* Creation of a new SQL pool operation might appear to have failed if your workspace name starts with a number. However, SQL pool is created successfully, the GRANT control setting would not have been applied correctly in this scenario. You need to follow the below steps to have the proper "Grant CONTROL" setting applied manually to your newly created SQL pools:

	* Click on "Launch Synapse Studio" in the portal
	* Click Data in the Left Navigation Panel and navigate to the SQL Pool that needs the setting in the Databases section
	* Invoke a "New SQL Script" on the SQL Pool 
	* To create a new workspace managed identity user and to assign control permissions to the user run the following in the pool: ```CREATE USER [WorkspaceName] FROM EXTERNAL PROVIDER``` ```GRANT CONTROL TO [WorkspaceName]```
	* To revoke control on the SQL Pool (Note that Synapse orchestration scenarios will not work if this run on this SQL Pool): ```REVOKE CONTROL TO [WorkspaceName]```
	* To drop Workspace managed identity user (Note that Synapse orchestration scenarios will not work if this run on this SQL Pool): ```DROP USER [WorkspaceName]```

## **Recommended Steps**

* Learn [how to troubleshoot](https://docs.microsoft.com/azure/synapse-analytics/troubleshoot/troubleshoot-synapse-studio#troubleshooting-steps) Synapse Studio
* Diagnose connectivity issues using this [PowerShell script](https://docs.microsoft.com/azure/synapse-analytics/troubleshoot/troubleshoot-synapse-studio-powershell)
* Confirm Synapse Studio is able to access all the required endpoints:

   - Make sure that the firewall on your network and local computer allows outgoing communication on TCP ports 80, 443 and 1443 for Synapse Studio
   - Allow outgoing communication on UDP port 53 for Synapse Studio
   - To connect using tools such as SSMS and Power BI, you must allow outgoing communication on TCP port 1433
   - If you're using the default Redirect connection policy setting, you may need to allow outgoing communication on additional ports

* Test access with different browsers and disable any pop-up blockers and plugins
* Investigate issues related to Security and Permissions:

	- [Workspaces, data, and pipelines](https://docs.microsoft.com/azure/synapse-analytics/sql/access-control)
   	- [Managed identities](https://docs.microsoft.com/azure/synapse-analytics/security/synapse-workspace-managed-identity)
	- [Database access](https://docs.microsoft.com/azure/azure-sql/database/logins-create-manage?toc=%2Fazure%2Fsynapse-analytics%2Ftoc.json&bc=%2Fazure%2Fsynapse-analytics%2Fbreadcrumb%2Ftoc.json)
	
## **Recommended Documents**

* [Launch Synapse Studio](https://docs.microsoft.com/azure/synapse-analytics/quickstart-synapse-studio#launch-synapse-studio)
* [Connect to Synapse from your own network](https://docs.microsoft.com/azure/synapse-analytics/security/synapse-workspace-ip-firewall#connect-to-synapse-from-your-own-network)
* [Synapse Workspace Pools and On Demand Inaccessible](https://techcommunity.microsoft.com/t5/azure-synapse-analytics/synapse-workspace-pools-and-on-demand-inaccessible/ba-p/1403485)
* [Managed Virtual Network](https://docs.microsoft.com/azure/synapse-analytics/security/synapse-workspace-managed-vnet)
* [Managed private endpoints](https://docs.microsoft.com/azure/synapse-analytics/security/synapse-workspace-managed-private-endpoints)
* [Azure roles to access blob and queue data](https://docs.microsoft.com/azure/storage/common/storage-auth-aad-rbac-portal?toc=/azure/synapse-analytics/toc.json&bc=/azure/synapse-analytics/breadcrumb/toc.json)
