<properties
	  pageTitle="Pages or blades won't load or Missing ResourcesDB - db collections are missing from your portal blades"
	  description="Pages or blades won't load or Missing ResourcesDB - db collections are missing from your portal blades"
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
	  articleId="4954a4d6-2f56-43d3-b8b9-97ca27573239"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Pages or blades won't load or Missing ResourcesDB - db collections are missing from your portal blades

<!--issueDescription-->
### ** THIS IS NOT A CUSTOMER READY CONTENT MESSAGE **

**Investigation (not customer message):**

#### Issue: 
- Resources are missing
- Pages or blades won't load  

**Symptom**:
- Databases or collections are missing from your portal blades
- Attempt to do CRUD operation on the database account results the following error on azure portal:
- Pages and blades in the portal do not display.  

**Solution**:
1. Lower application usage to operate under the maximum throughput quota for the collection. 
2. Check if the subscription is suspended.

**Explanation**: 

The portal is an application like any other, making calls to your DocumentDB database and collection. If your requests are currently being throttled due to calls being made from a separate application, the portal may also be throttled, causing resources not to appear in the portal. To resolve the issue, address the cause of the high throughput usage, and then refresh the portal blade. Information on how to measure and lower throughput usage can be found in the [Throughput](https://docs.microsoft.com/en-us/azure/cosmos-db/performance-tips#throughput) section of the [Peformance tips](https://docs.microsoft.com/en-us/azure/cosmos-db/performance-tips) article.
##KUSTO

**In?ternal info**:  
We can use a Kusto query like this to check the throttling situation for the account -

```
BackendEndRequest5M
| where TIMESTAMP >= now(-1d)
| where DocumentServiceId startswith "xxxxxxxxxxxx"
| where StatusCode == 429
| summarize sum(SampleCount) by bin(TIMESTAMP, 5m)
| order by TIMESTAMP desc
| render timechart
```

## Customer message:
Based on the troubleshooting step before, please write your conclusions to customer. Don't include any Kusto Query, you can share the output table but make sure to not incude any internal information.

<!--/issueDescription-->

