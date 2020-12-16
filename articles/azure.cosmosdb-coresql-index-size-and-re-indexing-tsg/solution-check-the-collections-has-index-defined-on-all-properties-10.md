<properties
	  pageTitle="Check the collections has Index Defined on all Properties"
	  description="Check the collections has Index Defined on all Properties"
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
	  articleId="a463e586-f1f1-42db-9ade-3e58172e407d"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Check the collections has Index Defined on all Properties

<!--issueDescription-->

The below query would provide return the below details

1. DefaultPathSpec : 4 =>  mean its custom index definition. Anyother value is /*
2. LastCompositePath: 4=> No Composite Index Defined 

```
MetricsIndexingPolicy5M
| where CollectionId == "D3wQALXlSQA=" and TIMESTAMP > now(-5d)
| summarize count() by TIMESTAMP, DefaultPathSpec, MaxIncludedPaths, MaxExcludedPaths, LastCompositePaths, LastCompositeSpecs, LastCompositeIndexDistribution, IndexingSchemeVersion, IndexingMode, LastSpatialPaths
| order by TIMESTAMP desc
```

**Customer message:**
Based on the troubleshooting step before, please write your conclusions to customer.Don't include any Kusto Query.

<!--/issueDescription-->

