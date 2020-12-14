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
	  articleId="f2d4e90b-3ff2-42fb-b65a-cabdbe5b3aab"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# How to find the account is enabled to enforce the TLS 1.2?

<!--issueDescription-->

Please kindly use the below Kusto query and check if the minimum_TLS column has the value 'Tls12':
```
MgmtDatabaseAccountTrace
| where TIMESTAMP > ago(4h)
| where ConfigurationOverrides contains "minimumTransportLayerSecurityLevel"
| where GlobalDatabaseAccount == "<customer's DB Account name>"
| extend minimum_TLS = parse_json(ConfigurationOverrides).minimumTransportLayerSecurityLevel
| summarize by GlobalDatabaseAccount, tostring(minimum_TLS)
```


**Customer message:**
Based on the troubleshooting step before, please write your conclusions to customer.Don't include any Kusto Query.

<!--/issueDescription-->

