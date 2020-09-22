<properties
  pagetitle="Generate and Retrieve Managed Identity for ADF"
  ms.author="chez,vimals"
  selfhelptype="Generic"
  supporttopicids="32629509"
  resourcetags=""
  productpesids="15613"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="eb28612d-639e-4bb9-9b59-bc8ae87dc1fb"
  ownershipid="AzureData_DataFactory" />
# Generate and Retrieve Managed Identity for ADF

Data factory service identity is based upon _managed identities for Azure resources_. For more information about managed identities, please refer to [Managed Identities for Azure Resources Overview](https://docs.microsoft.com/azure/active-directory/managed-identities-azure-resources/overview)

## **Recommended Steps** <br>

- **Missing Service Identity:** 
If you find that your data factory doesn't have a _service identity_ associated, following the steps in [_Retrieve managed identity_](https://docs.microsoft.com/azure/data-factory/data-factory-service-identity#retrieve-managed-identity) section. You can explicitly generate one following the steps in [_Generate managed identity_](https://docs.microsoft.com/azure/data-factory/data-factory-service-identity#generate-managed-identity) section. <br>

- **Moved Data Factory from one tenant to another**: If you've moved Data Factory from one tenant to another and receiving _InvalidResourceIdentityPrincipalId_ error, try generating a new managed identity to resolve it. You can use Powershell or the REST API as mentioned in [_Generate service identity_](https://docs.microsoft.com/azure/data-factory/data-factory-service-identity#generate-service-identity), below are the steps when using powershell: <br>

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
<br>

## **Recommended Documents**

Azure Data Factory Service Identity [Document](https://docs.microsoft.com/azure/data-factory/data-factory-service-identity), including following sections: <br>

* [Retrieve service identity](https://docs.microsoft.com/azure/data-factory/data-factory-service-identity#retrieve-service-identity) <br>
* [Generate service identity](https://docs.microsoft.com/azure/data-factory/data-factory-service-identity#generate-service-identity) <br>