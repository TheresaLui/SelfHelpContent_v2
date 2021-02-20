<properties
  pagetitle="V2 - Pipeline Activities - Databricks&#xD;"
  service=""
  resource=""
  ms.author="chez,haoc,rakatuko,dfandel"
  selfhelptype="Generic"
  supporttopicids="32629480"
  resourcetags=""
  productpesids="15613"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="3d7b6288-51d3-4d2d-b4f7-0822b21160f5"
  ownershipid="AzureData_DataFactory" />
# V2 - Pipeline Activities - Databricks

## **Recommended Steps**

* If you've received an error message from Databricks activities, including Jar, Notebook, and Python activity, see the [ADF Troubleshooting Guide to understand error codes](https://docs.microsoft.com/azure/data-factory/data-factory-troubleshoot-guide#azure-databricks)

* If your Databricks Notebook Activity is running for a longer period or failed: Because this is a customer-owned cluster, go to the Databricks account or URL provided in the pipeline to find the cluster logs for more details about the error.

* An error code of 3200 with a 403 error usually indicates your Databricks access token might be expired.  [Access Token Generation Instructions](https://docs.azuredatabricks.net/api/latest/authentication.html#generate-a-token)

* Error codes of 3201 usually indicate an authoring error.

* An error code of 3204 with a "Could not launch cluster due to cloud provider failures" message usually indicates an insufficient quota of cores. Request for increase of core quota per guidance [here](https://docs.microsoft.com/azure/azure-portal/supportability/per-vm-quota-requests)

## **Recommended Documents**

* Activities documents, including:
  * [Databricks documents](https://docs.microsoft.com/azure/databricks/)
  * Databricks [Jar Activity](https://docs.microsoft.com/azure/data-factory/transform-data-databricks-jar)
  * Databricks [Notebook Activity](https://docs.microsoft.com/azure/data-factory/transform-data-databricks-notebook)
  * Databricks [Python Activity](https://docs.microsoft.com/azure/data-factory/transform-data-databricks-python)

* Other document
  * Transform data in the cloud with [Databricks Notebook Activity](https://docs.microsoft.com/azure/data-factory/transform-data-using-databricks-notebook)
  * [Databricks Linked Services](https://docs.microsoft.com/azure/data-factory/compute-linked-services#azure-databricks-linked-service)
  * [Databricks Solution Template](https://docs.microsoft.com/azure/data-factory/solution-template-databricks-notebook)

**Azure Data Factory Information** 

* [Azure Data Factory Updates](https://azure.microsoft.com/updates/?query=factory)
* [Azure Data Factory Blog](https://techcommunity.microsoft.com/t5/azure-data-factory/bg-p/AzureDataFactoryBlog)
* [Azure Data Factory FAQ](https://docs.microsoft.com/azure/data-factory/frequently-asked-questions)
* [Azure Data Factory Troubleshooting Guide](https://docs.microsoft.com/azure/data-factory/data-factory-troubleshoot-guide)
* [Feature Request](https://feedback.azure.com/forums/270578-azure-data-factory)