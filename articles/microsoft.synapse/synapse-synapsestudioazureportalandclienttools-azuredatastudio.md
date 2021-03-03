<properties
  pagetitle="Synapse Studio, Azure Portal and Client Tools/Azure Data Studio"
  service="microsoft.synapse"
  resource="sqlpools"
  ms.author="saltug,goventur"
  selfhelptype="Generic"
  supporttopicids="32738759"
  resourcetags=""
  productpesids="15818"
  cloudenvironments="public,fairfax,blackforest,mooncake,usnat,ussec"
  articleid="synapse-synapsestudioazureportalandclienttools-azuredatastudio"
  ownershipid="AzureData_SQLDataWarehouse" />
# Synapse Studio, Azure Portal and Client Tools/Azure Data Studio

## **Recommended Steps**

* To connect and query SQL pool using Azure Data Studio, follow [steps outlined here](https://docs.microsoft.com/sql/azure-data-studio/quickstart-sql-dw?view=sql-server-2017). Make sure to set the firewall rule allowing Azure Data Studio to connect as explained in the tutorial.
* Install the [latest version of ADS](https://docs.microsoft.com/sql/azure-data-studio/download-azure-data-studio?view=azure-sqldw-latest)
* Check for known issues and bug fixes in the [Release notes](https://docs.microsoft.com/sql/azure-data-studio/release-notes-azure-data-studio?view=sql-server-ver15)
* Ensure all ADS Extensions are up to date
* [Azure Data Studio support for Azure Synapse](https://docs.microsoft.com/sql/azure-data-studio/faq?view=sql-server-ver15#does-azure-data-studio-integrate-with-azure-sql-data-warehouse) is currently in public preview, some features might not be available yet. Review the [supported features & comparison between ADS and SSMS](https://docs.microsoft.com/sql/azure-data-studio/what-is?view=sql-server-ver15#feature-comparison-with-sql-server-management-studio-ssms).
* Unsupported features specific to Azure Synapse:

  - SQL Profiler

* Search for known issues in [GitHub for ADS](https://github.com/microsoft/azuredatastudio/issues?q=is%3Aissue+is%3Aopen)
* When should I use [ADS vs SSMS](https://docs.microsoft.com/sql/azure-data-studio/faq?view=sql-server-2017#when-should-i-use-azure-data-studio-vs-sql-server-management-studio)?
* How to [enable tracing in ADS](https://github.com/microsoft/azuredatastudio/wiki/Troubleshooting-Issues) to capture diagnostic logs
* Submit an [idea or recommendation](https://github.com/microsoft/azuredatastudio/wiki/Submitting-Bugs-and-Suggestions) to improve Azure Data Studio
