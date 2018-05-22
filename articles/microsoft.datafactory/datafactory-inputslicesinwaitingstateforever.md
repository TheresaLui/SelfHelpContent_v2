<properties 
	pageTitle="Input slices are in Waiting state for ever" 
	description="Input slices are in waiting state for ever." 
	service="microsoft.datafactory" 
	resource="datafactories"
	authors="spelluru"
	displayOrder="2"
	selfHelpType="resource"
	cloudEnvironments="public"
    supportTopicIds="32356674"
    productPesIds="15613"
    resourceTags=""
/>

# Input slices are in Waiting state for ever

## **Recommended steps**
The slices could be in **Waiting** state due to a number of reasons and one of the common reasons is that the **external** property is not set to **true**. Any dataset that is produced outside the scope of Azure Data Factory should be marked with **external** property . This indicates that the data is external and not backed by any pipelines within the data factory. The data slices are marked as **Ready** once the data is available in the respective store. 

See the following example for the usage of the **external** property. You can optionally specify **externalData*** when you set external to true.. 

See [Datasets](https://azure.microsoft.com/documentation/articles/data-factory-create-datasets/) article for more details about this property.

	{
	  "name": "CustomerTable",
	  "properties": {
	    "type": "AzureBlob",
	    "linkedServiceName": "MyLinkedService",
	    "typeProperties": {
	      "folderPath": "MyContainer/MySubFolder/",
	      "format": {
	        "type": "TextFormat",
	        "columnDelimiter": ",",
	        "rowDelimiter": ";"
	      }
	    },
	    "external": true,
	    "availability": {
	      "frequency": "Hour",
	      "interval": 1
	    },
	    "policy": {
	      }
	    }
	  }
	}

To resolve the error, add the **external** property and the optional **externalData** section to the JSON definition of the input table and recreate the table. 

## **Recommended documents**
[Monitor and Manage Azure Data Factory pipelines](https://azure.microsoft.com/documentation/articles/data-factory-monitor-manage-pipelines/)<br>
[Scheduling and Execution](https://azure.microsoft.com/documentation/articles/data-factory-scheduling-and-execution/)
