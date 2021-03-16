<properties
  pagetitle="Store Credentials in Azure Key Vault and use them in Azure Data Factory"
  description="Store credentials for data store and computes in AKV"
  ms.author="chez,susabat"
  selfhelptype="Generic"
  supporttopicids="32629445"
  resourcetags=""
  productpesids="15613"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="e77e0014-d0cb-4d49-a8e5-b5fc904811c2"
  ownershipid="AzureData_DataFactory" />
# Store Credentials in Azure Key Vault and use them in Azure Data Factory

Following this article, users are able to solve various credential related issues in Azure Key Vault and use them in Azure Data Factory.

__Note__: This feature relies on data factory service identity. Please make sure your data factory has one associated. See [_ADF Service Identity_](https://docs.microsoft.com/azure/data-factory/data-factory-service-identity) for how to generate and retrieve ADF service identity.

## **Recommended Steps**

To reference a stored credential stored in Azure Key Vault, you need to:

1. Retrieve data factory service identity
1. Grant the service identity access to your Azure Key Vault
1. Create a linked service pointing to your Azure Key Vault
1. Create data store linked service, inside which reference the corresponding secret stored in key vault

Some cloud application services like *Xero* linked services do not require expression type wehre as *ADLSGen2, Databricks, Storage etc.*  require expression types.

For example, in a linked service of type Xero, the syntax that works is:



    "consumerKey": {
       "type": "AzureKeyVaultSecret",
       "store": {
       "referenceName": "dynamicKeyVault",
       "type": "LinkedServiceReference",
       "parameters": {
          "keyVaultUrl": {
    
             "value": "@{linkedService().keyVaultUrl}"
             }
    
          }
       },
    
       "secretName": "XeroAppClientId"
    }


 

whereas to use the same dynamic Key Vault, the syntax for a linked service of type ADLS Gen2 is:

    "url": {
       "type": "AzureKeyVaultSecret",
       "store": {
       "referenceName": "dynamicKeyVault",
       "type": "LinkedServiceReference",
    
       "parameters": {
          "keyVaultUrl": {
               "value": "@linkedService().keyVaultUrl",
                "type": "Expression"
                }
          }
    
       },
       "secretName": "DataLakeStoreUrl"
    
    }



 Store credentials in and retrieve from Azure Key Vault [Document](https://docs.microsoft.com/azure/data-factory/store-credentials-in-key-vault). 
 
## **Recommended Documents**

* [Prerequisites](https://docs.microsoft.com/azure/data-factory/store-credentials-in-key-vault#prerequisites)
* [Steps](https://docs.microsoft.com/azure/data-factory/store-credentials-in-key-vault#steps) 
* [Azure Key Vault linked service](https://docs.microsoft.com/azure/data-factory/store-credentials-in-key-vault#azure-key-vault-linked-service) 
* [Reference secret stored in key vault](https://docs.microsoft.com/azure/data-factory/store-credentials-in-key-vault#reference-secret-stored-in-key-vault)