<properties 
    pageTitle="Diagnose and resolve issues with Delta Streaming" 
    description="Diagnose and resolve issues with Delta Streaming" 
    service="microsoft.databricks" 
    resource="workspaces" 
    authors="lahaddad" 
    ms.author="lahaddad" 
    displayOrder="15" 
    selfHelpType="generic" 
    supportTopicIds="32784342" 
    resourceTags="" 
    productPesIds="16432" 
    cloudEnvironments="public, fairfax, usnat, ussec" 
    articleId="a001e950-b34d-412d-8cda-0b06d45c6f1f" 
    ownershipId="AzureData_AzureDatabricks" 
/> 

# Diagnose and resolve issues with Delta Streaming 

## **Recommended Steps**

* [Concurrency Control](https://docs.microsoft.com/azure/databricks/delta/concurrency-control)

* When a transaction conflict occurs, you will observe one of the following exceptions:

  * [ConcurrentAppendException](https://docs.microsoft.com/azure/databricks/delta/concurrency-control#concurrentappendexception)
  * [ConcurrentDeleteReadException](https://docs.microsoft.com/azure/databricks/delta/concurrency-control#concurrentdeletereadexception)
  * [ConcurrentDeleteDeleteException](https://docs.microsoft.com/azure/databricks/delta/concurrency-control#concurrentdeletedeleteexception)
  * [MetadataChangedException](https://docs.microsoft.com/azure/databricks/delta/concurrency-control#metadatachangedexception)
  * [ConcurrentTransactionException](https://docs.microsoft.com/azure/databricks/delta/concurrency-control#concurrenttransactionexception)
  * [ProtocolChangedException](https://docs.microsoft.com/azure/databricks/delta/concurrency-control#protocolchangedexception)


## **Recommended Documents** 

* [Azure Databricks Platform release notes](https://docs.microsoft.com/azure/databricks/release-notes/product/) cover the features that we develop for the Azure Databricks platform 
* [Databricks Runtime release notes](https://docs.microsoft.com/azure/databricks/release-notes/runtime/) cover the features that we develop for Databricks cluster runtimes or images. This includes proprietary features and optimizations. 
* [Delta FAQs](https://docs.microsoft.com/azure/databricks/delta/delta-faq) 
* [Delta How-to?](https://docs.microsoft.com/azure/databricks/delta/delta-intro) 
* [Resources](https://docs.microsoft.com/azure/databricks/delta/delta-resources) 
* [Best Practices](https://docs.microsoft.com/azure/databricks/delta/best-practices) 
* [Delta Lake Tips and Troubleshooting](https://docs.microsoft.com/azure/databricks/kb/delta/) 
* [Introductory Notebooks](https://docs.microsoft.com/azure/databricks/delta/intro-notebooks) 
