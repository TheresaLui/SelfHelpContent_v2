<properties
	  pageTitle="Know if a physical partition split is currently taking place"
	  description="Know if a physical partition split is currently taking place"
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
	  articleId="c846e8eb-2145-4e2c-bb6d-851bab75d0df"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Know if a physical partition split is currently taking place

<!--issueDescription-->
### ** THIS IS NOT A CUSTOMER READY CONTENT MESSAGE **

**Next steps:** One common CRI is that customers will report, "My scale-up operation seems to be taking a while. What should I do?". We should first check if the split operation is pending, via the **IsOfferReplacePending** property in **BillingOffers5M**.

```
let _collectionname="xxxxxx";
let _globaldatabasename="xxxxxx";
let _ago =2d;
BillingOffers5M | where TIMESTAMP > ago(_ago) | where IsSharedThroughputOffer ==0
| where CollectionName == _collectionname?  and GlobalDatabaseAccountName ==_globaldatabasename
| summarize  min(TIMESTAMP), max(TIMESTAMP) by GlobalDatabaseAccountName, CollectionName, CollectionRid,IsOfferReplacePending,ProvisionedThroughputCapacity
| order by min_TIMESTAMP asc nulls last
```

Check the partition count:
```
let _collectionname="xxxxxxxxxxxx";
let _globaldatabasename="xxxxxxxxxxxx";
ReportQuota5M | where CollectionName ==_collectionname and GlobalDatabaseAccountName ==_globaldatabasename and TIMESTAMP > datetime(2019-10-23 01:15:00.0000000) and TIMESTAMP <=datetime(2019-10-23 21:00:00.0000000)
| summarize dcount(PartitionId) by GlobalDatabaseAccountName, CollectionName, CollectionRid
```

## Customer message:
Based on the troubleshooting step before, please write your conclusions to customer. Don't include any Kusto Query, you can share the output table but make sure to not incude any internal information.

<!--/issueDescription-->

