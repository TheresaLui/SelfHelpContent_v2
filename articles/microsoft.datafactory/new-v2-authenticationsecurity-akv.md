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

**Note**: This feature relies on data factory service identity. Make sure that your data factory has one associated with it. To generate and retrieve ADF service identity, see [ADF Service Identity](https://docs.microsoft.com/azure/data-factory/data-factory-service-identity).

## **Recommended Steps**

To reference a stored credential stored in Azure Key Vault:

1. Retrieve the data factory service identity
1. Grant the service identity access to your Azure Key Vault
1. Create a linked service pointing to your Azure Key Vault
1. Create a data store linked service, inside which references the corresponding secret stored in key vault

Some cloud application services, like Xero linked services, don't require expression types. ADLSGen2, Databricks, and Storage do require expression types.

For example, in a linked service of type Xero, the correct syntax is as follows:


```
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
```
 

Whereas, to use the same dynamic Key Vault, the correct syntax for a linked service of type ADLS Gen2 is:

```
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
```

 Store your credentials in--and retrieve them from--Azure Key Vault. [See more details](https://docs.microsoft.com/azure/data-factory/store-credentials-in-key-vault). 
 
## **Recommended Documents**

* [Key Vault prerequisites](https://docs.microsoft.com/azure/data-factory/store-credentials-in-key-vault#prerequisites)
* [Key Vault steps](https://docs.microsoft.com/azure/data-factory/store-credentials-in-key-vault#steps) 
* [Azure Key Vault linked service](https://docs.microsoft.com/azure/data-factory/store-credentials-in-key-vault#azure-key-vault-linked-service) 
* [Reference secret stored in key vault](https://docs.microsoft.com/azure/data-factory/store-credentials-in-key-vault#reference-secret-stored-in-key-vault)
