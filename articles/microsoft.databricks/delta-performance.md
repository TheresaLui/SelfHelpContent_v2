<properties 
    pageTitle="Diagnose and resolve issues with Delta Performance" 
    description="Diagnose and resolve issues with Delta Performance" 
    service="microsoft.databricks" 
    resource="workspaces" 
    authors="lahaddad" 
    ms.author="lahaddad" 
    displayOrder="15" 
    selfHelpType="generic" 
    supportTopicIds="32784341" 
    resourceTags="" 
    productPesIds="16432" 
    cloudEnvironments="public, fairfax, usnat, ussec" 
    articleId="451f6001-cada-46f2-8b3a-472b51456452" 
    ownershipId="AzureData_AzureDatabricks" 
/> 

 
# Diagnose and resolve issues with Delta Performance 
 
## **Recommended Steps**

* **Delta table query performance is slow when underlying data directory is in ADLS Gen2 filesystem** - This issue affects clusters on Databricks Runtime 5.4 or earlier because these versions check for the latest version of a Delta Lake table on ADLS Gen2 by listing all available versions, and then find the latest version of the Delta table.

In DBR 5.5, only the end of the transaction log is checked instead of listing all available versions. This optimization significantly improves the latency. For better Delta table query performance, use DBR 5.5 or above.

## **Recommended Documents** 

* [Azure Databricks Platform release notes](https://docs.microsoft.com/azure/databricks/release-notes/product/) cover the features that we develop for the Azure Databricks platform 
* [Databricks Runtime release notes](https://docs.microsoft.com/azure/databricks/release-notes/runtime/) cover the features that we develop for Databricks cluster runtimes or images. This includes proprietary features and optimizations. 
* [Delta FAQs](https://docs.microsoft.com/azure/databricks/delta/delta-faq) 
* [Delta How-to?](https://docs.microsoft.com/azure/databricks/delta/delta-intro) 
* [Resources](https://docs.microsoft.com/azure/databricks/delta/delta-resources) 
* [Best Practices](https://docs.microsoft.com/azure/databricks/delta/best-practices) 
* [Delta Lake Tips and Troubleshooting](https://docs.microsoft.com/azure/databricks/kb/delta/) 
* [Introductory Notebooks](https://docs.microsoft.com/azure/databricks/delta/intro-notebooks) 
