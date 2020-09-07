<properties
	pageTitle="V2 - Authoring and Development - Cannot Publish"
	description="V2  - Authoring and Development - Cannot Publish"
	service=""
	resource=""
	authors="hecepeda"
	ms.author="hecepeda"
	displayOrder=""
	selfHelpType="generic"
    supportTopicIds="32629446"
	resourceTags=""
	productPesIds="15613"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="datafactory-v2-authoring-development-issues-cannot-publish.md"
	ownershipId="AzureData_DataFactory"
/>

# V2 Data Factory - Cannot Publish Changes

## **Recommended Steps**

* Ensure [roles and permissions are set up properly](https://docs.microsoft.com/azure/data-factory/concepts-roles-permissions)

### __Common Errors__

**InvalidResourceIdentityPrincipalId**: The Data Factory does not contain a managed identity. This could be caused by moving resources across tenants.

If you see this error after performing a change on your Data Factory, you can try generating a new managed identity to resolve it. You can use Powershell or the REST API as mentioned in [_Generate service identity_](https://docs.microsoft.com/azure/data-factory/data-factory-service-identity#generate-service-identity), below are the steps when using powershell:

* **Install Powershell AZ module, connect to Azure and select the subscription hosting your Data Factory**:

```
Install-Module -Name Az -AllowClobber
Connect-AzAccount
Get-AzSubscription -SubscriptionName "MyProdSubscription"
Select-AzSubscription -SubscriptionName "your subscription name" 
```

* **Execute cmdlet to create new managed Identity**: 

```
PS C:\WINDOWS\system32> Set-AzDataFactoryV2 -ResourceGroupName <resourceGroupName> -Name <dataFactoryName> -Location <region>

DataFactoryName   : ADFV2DemoFactory
DataFactoryId     : /subscriptions/<subsID>/resourceGroups/<resourceGroupName>/providers/Microsoft.DataFactory/factories/ADFV2DemoFactory
ResourceGroupName : <resourceGroupName>
Location          : East US
Tags              : {}
Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
ProvisioningState : Succeeded
```

## **Recommended Documents**

- How to: [Troubleshooting Git Integration](https://docs.microsoft.com/azure/data-factory/source-control#troubleshooting-git-integration)

**FAQ**

- [ADF FAQ](https://docs.microsoft.com/azure/data-factory/frequently-asked-questions)
- [Feature Request](https://feedback.azure.com/forums/270578-azure-data-factory)
