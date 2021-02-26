<properties
	  pageTitle="Check the history of physical partitions over time"
	  description="Check the history of physical partitions over time"
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
	  articleId="3b89a704-fe38-4994-ac48-ec6b5ceae939"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Check the history of physical partitions over time

<!--issueDescription-->
### ** THIS IS NOT A CUSTOMER READY CONTENT MESSAGE **

**Next steps:** 

[Number of physical partitions for manual throughput collection](https://cosmosdbmetrics.kusto.windows.net/MetricsDB?query=H4sIAAAAAAAEAH1STU8bQQy9R%2bp%2fsOghiRSSFM5Bgmyr9gCN%2bLqiyayTsTof0XimyVb98Xh3YbMCxNzG9nt%2bfvZs1r0CE0ZHnvwWvkLYwM5UTFpZ2KmYKFHwDJsQwSmfJZpMDHlrdjmBDtaibiuOhLMvA20zC%2btoqAO7wOXaYYqkefpH4mG6J1%2bGPU89puF4Wqqk1opxNLxuq4oriRaKbLXsGtxl51SsHs8G%2f2FvMCIUKiFcLEBtw%2bh8Pi%2fHIgHuDTEInUUwiuEbVKhiPVTdBE6BEkiBkq%2bwA7ekdR6VNr15JrCnZARvyaOg0DUWNFURt1IhPmAPUNOS74trZrrUOmSfbpRDWCzgZNn4UVw99RInHeoXX%2bYU7sR7%2fO7rIcoaNO%2fy1%2brwM%2bRoq1UMf4mlLZb3x3VcwFw8%2bEFWrIfwZj%2fkgY2KQtlb4Kv1LC1aM%2bgfwk12a4y%2fN6uXQ1gd72AhV3AYFcSJvE5dYlnPMp7Ax7pa0Ofix7CuOtdqVyZwXP7b%2fy2Vk2b%2fIhsPCX0Jtw%2b8wvhOsfT%2bWNPskykHg2eNgCI5HwMAAA%3d%3d&web=0)
```
/////////// Determining # of physical partitions for manual throughput collections ///////////
cluster('cosmosdbmetrics.kusto.windows.net').database('MetricsDB').DailyCollectionSummaryV2
| where Date >= ago(300d) // This table has 1 year of data - it is a daily summary of each collection, with 1 line item for each region the collection is in
| where DatabaseAccountName == "CosmosDB_AccountName"
| where IsAutoScaleEnabled == 0
| where MaxHourlyProvisionedThroughput > 0 //Filter out collections in shared throughput databases
| summarize NumberOfPhysicalPartitions = max(DistinctPartitionCount), ProvisionedThroughput = max(MaxHourlyProvisionedThroughput) by DatabaseName, CollectionName, CollectionRid, Date
| extend RUsPerPhysicalPartition = ProvisionedThroughput / NumberOfPhysicalPartitions
```

[Number of physical partitions for autoscale collection](https://cosmosdbmetrics.kusto.windows.net/MetricsDB?query=H4sIAAAAAAAEAH1Sy27bMBC8C8g%2fLNKDbcC1nObsAI7Voj3ENZzHtVhTa2tRiTRIKrKKfnyXVGIpDVreuLOvmdk0Pb%2bMPNmKNesDfACzh2PROlZYwhGtZ89GO9gbC1h74yROoExZkuqQvlGaqLJ20mw8UsZVxuW7irxl5WY%2fJW5mDevcNG6myY8msxw97tDReHTXZWW3Es2Qy3Z17n9fVxXa9unTRfIbmoIsQYae4GYBeDDj6%2fk8n8gK8FCwA%2bknyxXo4ApaQhvIhCnwEdiDJKB8pT24rmvACVUx4DOFhn0h9SVrkiqqIvWYZekgGeCLoQChLes320VWS6VMrf0aK4LFAi5XUZHs9scAuOzLvrmlqHsf1P2sA408VF0B6hyWr7o%2fkXVhpCDXfekdnr6a2pbtxppnDgmUPxTW1IfiWHu4gbkI9IVLMQaMBIbmsQZXoJVpvq94NcZdJKLs2ojcDUHtKFLvr6DCE2wfU9HdgKMO1XW1oyh8RPBZ9I6uyNpRxPfHFZh0hvAvgnVs8H2%2fecnb9De4CBPHGTvPWvkzsApyTqa9TCLIgH9XJbGAH7k0%2fg0%2bgV17Ni2YMoX%2b%2bv7%2bbzmfxvsLO9PJk7izfXQbsu%2fWlbn%2fWCj9D8ck%2bQO4UTAFmQMAAA%3d%3d&web=0)

```
/////////// Determining # of physical partitions for autoscale collections ///////////
cluster('cosmosdbmetrics.kusto.windows.net').database('MetricsDB').DailyCollectionSummaryV2
| where Date >= ago(300d) // This table has 1 year of data - it is a daily summary of each collection, with 1 line item for each region the collection is in
| where DatabaseAccountName == "CosmosDB_AccountName"
| where IsAutoScaleEnabled == 1 and AutoscaleVersion == 3
| where MaxHourlyProvisionedThroughput > 0 //Filter out collections in shared throughput databases
// Note we use the autoscale max RU/s to see the number of RU/s available on each physical partition
| summarize NumberOfPhysicalPartitions = max(DistinctPartitionCount), AutoscaleMaxThroughput = max(MaxAutopilotMaxThroughput) by DatabaseName, CollectionName, CollectionRid, Date
| extend RUsPerPhysicalPartition = AutoscaleMaxThroughput / NumberOfPhysicalPartitions
```

[Number of physical partitions for shared throughput database](https://cosmosdbmetrics.kusto.windows.net/MetricsDB?query=H4sIAAAAAAAEAH1Ry04CQRC88xUdPAAJAuoZE2BN9AASMV7NMNswHedB5iGs8ePtWXThoM6tu7pqqquHw%2bYVGNEbsmS3cAFuAztVBZJCw074SJGcDbBxHoywibtBCY8lROVd2qpdilCKKNYiYICT6rAldQqs3O1IF4wL5dpg9CTD4I37brAnW7p9GFiMnd7gR6LbmR%2bniil3C0G6Kr6hVTJG%2bOrluvUJe4UegRGE2zGIrevejEZlj%2f%2bHZ0UBmKERlAhwBRUKn9fKX8AlUAQeEFyyNoSjaMZRSAXSaY0y79yHPUXFfE0WmYWmDqGe8rjlCY4AzwhZluy5udr2REqXbFwIgzAeQ3tWp1FMX8%2bAdsOai8O9S15XS%2b%2feKbAsls%2bnpG9HvOKGNOcK0YGzeYW%2f79HIPoRJim7FR8U7m7Mps5cR48cA6ANhkcwa%2feNm%2bX3%2b5en6Y779oVtQiGRlbIBZ9t%2frw%2b9ej6T%2fF%2brBumqSykn0m%2bqJyrrAVusLObcms60CAAA%3d&web=0)

```
/////////// Determining # of physical partitions for manual shared throughput databases ///////////
cluster('cosmosdbmetrics.kusto.windows.net').database('MetricsDB').DailyDatabaseSummaryV2
| where Date >= ago(300d) // This table has 1 year of data - it is a daily summary of each collection, with 1 line item for each region the collection is in
| where DatabaseAccountName == "CosmosDB_AccountName"
| where MaxHourlyProvisionedThroughput >0 //filter to only shared throughput databases
| where IsAutoScaleEnabled == 0
| summarize NumberOfPhysicalPartitions = max(DistinctPartitionCount), ProvisionedThroughput = max(MaxHourlyProvisionedThroughput) by DatabaseName, DatabaseRid, Date
```

[Number of physical partitions for autoscale shared throughput database](https://cosmosdbmetrics.kusto.windows.net/MetricsDB?query=H4sIAAAAAAAEAH1STW%2fbMAy9B8h%2fILpDEiCL0%2fWcAmldYDs0C9KP66DITETUlgJRruNhP36U3MYZis4365GPj%2b8xy05fjgF9RZbsHr6A28HBtExalXBQPlAgZxl2zoOqg2N5R2CjPBYQjHf13hzqAIUKaqsYGXribKDLmoV8PNKOK8fFtsLgSfPsRd7drCFbuIZnFsNoMnunGI%2fuu6r8Rl5zRWWbv0EPdVUp3z5%2fG%2fyBxqBHEAThegFq78ZX83kxkfnwaIhBOkSpUQyX0KLycbM4Ar4CBZACJb%2fCDdyRRhyVNqBdWaKOa0%2bhoWCkvySL0oVV8iFVedxLhViAZw2RluzwXF3SvdTa1TasVIWwWMDFbbIjv%2fl1Blz0bffq%2bN3VvmzX3r0SCzEWj73X13NZckelOAvBgbNxic8T6Xl%2f8FIifIgR3tloTxHVXIKyBSzfw31GHydG5Go4EDdXTixuEGrGtG5%2fBpU6wuYp46iCsUNtXW0xmZ0Q9SoepySEMhn38bqiwC4E%2bo2wSgQ%2fd%2bu3unV%2fhIs4cZwTB7I6nIDbaOFk2q8g%2fp3Z1XXJW8QPVLrwDz6BbXsKKgYxPf1tqJhCd2JRIx4DilObJ16j%2fyBP5nwiIPvPTsPBXxFWT7%2bKAwAA&web=0)


```
///////////Determining # of physical partitions for autoscale shared throughput databases ///////////
cluster('cosmosdbmetrics.kusto.windows.net').database('MetricsDB').DailyDatabaseSummaryV2
| where Date >= ago(300d) // This table has 1 year of data - it is a daily summary of each collection, with 1 line item for each region the collection is in
| where DatabaseAccountName == "CosmosDB_AccountName"
| where MaxHourlyProvisionedThroughput >0 //filter to only shared throughput databases
| where IsAutoScaleEnabled == 1 and AutoscaleVersion == 3
// Note we use the autoscale max RU/s to see the number of RU/s available on each physical partition
| summarize NumberOfPhysicalPartitions = max(DistinctPartitionCount), AutoscaleMaxThroughput = max(MaxAutopilotMaxThroughput) by DatabaseName, DatabaseRid,  Date 
| extend RUsPerPhysicalPartition = AutoscaleMaxThroughput / NumberOfPhysicalPartitions
```

## Customer message:
Based on the troubleshooting step before, please write your conclusions to customer.Don't include any Kusto Query, you can share the output table but make sure to not incude any internal information.

<!--/issueDescription-->

