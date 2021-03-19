<properties
	  pageTitle="How to find the account is enabled to enforce the TLS 1.2?"
	  description="How to find the account is enabled to enforce the TLS 1.2?"
      service="Microsoft.DocumentDB"
      resource="databaseAccounts"
	  authors="anferrei"
	  ms.author="anferrei"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="9c5c8f1e-75f1-4801-924f-ded9ae374926"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# How to find the account is enabled to enforce the TLS 1.2?

<!--issueDescription-->
### ** THIS IS NOT A CUSTOMER READY CONTENT MESSAGE **

**Next steps:** 
Please kindly use the below Kusto query and check if the minimum_TLS column has the value 'Tls12':
```
MgmtDatabaseAccountTrace
| where TIMESTAMP > ago(4h)
| where ConfigurationOverrides contains "minimumTransportLayerSecurityLevel"
| where GlobalDatabaseAccount == "<customer's DB Account name>"
| extend minimum_TLS = parse_json(ConfigurationOverrides).minimumTransportLayerSecurityLevel
| summarize by GlobalDatabaseAccount, tostring(minimum_TLS)
```


## Customer message:
Based on the troubleshooting step before, please write your conclusions to customer. Don't include any Kusto Query.

<!--/issueDescription-->

