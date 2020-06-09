<properties
    pageTitle="Create Data Share Account"
    description="Common root causes for data share account creation issues"
    service="microsoft.datashare"
    resource="shares"
    authors="desarkar"
    ms.author="desarkar"
    displayOrder=""
    selfHelpType="Generic"
    supportTopicIds="32675618, 32675622"
    resourceTags=""
    productPesIds="16762"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="datashare-create-datashareaccount"
	ownershipId="AzureData_DataShare"
/>

# Create Data Share Account

## **Recommended Steps**

### Permission Issues

Permissions issues may apply if you are facing any of these error messages during data share account creation:

* Error: Operation returned an invalid status code BadRequest
* Error: Authorization Failed
* Error: Role assignment to storage account
* Error: 1 datasets were not added because you do not have the required permissions to share 
* Error: `Caller does not have write privileges on resource: [subscriptions/]`
	
If you receive any of the above errors when creating a new data share or receiving a new data share, it is because there are insufficient permissions to the storage account. The permission required is "Microsoft.Authorization/role assignments/write", which exists in the storage owner role or can be assigned to a custom role. Even if you created the Storage account, it does NOT automatically make you the owner of the storage account. Follow these steps to grant yourself owner of the storage account. Alternatively, a custom role can be created with this permission that you can add yourself in to:
	
1. Navigate to Storage account in Azure portal
2. Select Access control (IAM)
3. Click Add
4. Add yourself in as owner

In the case of adding a dataset from a SQL Server, you must run a script which creates a new user in the database for the Data Share MSI. Note that you must be logged in as an AAD Admin via Query Editor (preview) to run this script.
 
`create user [datashareaccountname] from external provider; exec sp_addrolemember db_owner, [datashareaccountname];`
 
Note that the [datashareaccountname] must be the same name as your Data Share resource. 
 
### Resources have locks which impact account creation

* Please ensure that there are no [locks on your Resource Group](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-lock-resources)

### Service Outage

   * Check [Azure Status](https://status.azure.com/status) for any potential outages or service issues

## **Recommended Documents**

* [Error when creating or receiving a new Data Share](https://docs.microsoft.com/azure/data-share/data-share-troubleshoot#error-when-creating-or-receiving-a-new-data-share)<br>
* [Troubleshooting SQL-based sharing](https://docs.microsoft.com/azure/data-share/data-share-troubleshoot#troubleshooting-sql-based-sharing) 
