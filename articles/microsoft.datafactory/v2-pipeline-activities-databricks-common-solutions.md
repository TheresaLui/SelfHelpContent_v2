<properties
  pagetitle="V2 - Pipeline Activities - Databricks"
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

* If you are having authentication issues your DataBricks access token might be expired.  [Generation Instructions](https://docs.azuredatabricks.net/api/latest/authentication.html#generate-a-token)

## **Recommended Documents**

* Activities documents, including:
  * [Databricks documents](https://docs.microsoft.com/en-us/azure/databricks/)
  * Databricks [Jar Activity](https://docs.microsoft.com/azure/data-factory/transform-data-databricks-jar)
  * Databricks [Notebook Activity](https://docs.microsoft.com/azure/data-factory/transform-data-databricks-notebook)
  * Databricks [Python Activity](https://docs.microsoft.com/azure/data-factory/transform-data-databricks-python)

* Other document
  * Transform data in the cloud with [Databricks Notebook Activity](https://docs.microsoft.com/azure/data-factory/transform-data-using-databricks-notebook)
  * [Databricks Linked Services](https://docs.microsoft.com/en-us/azure/data-factory/compute-linked-services#azure-databricks-linked-service)
  * [Databricks Solution Template](https://docs.microsoft.com/en-us/azure/data-factory/solution-template-databricks-notebook)