<properties
    pageTitle="Copy Activity - Schema Mapping"
    description="Schema mapping in copy activity"
    infoBubbleText=""
    authors="chez-charlie"
    ms.author="chez"
    articleId="dcce5834-ba0a-4d8e-94ad-13549b5b8e6a"
    diagnosticScenario=""
    selfHelpType="generic"
    supportTopicIds="32629469"
    resourceTags=""
    productPesIds="15613"
    cloudEnvironments="public"
/>

# Schema Mapping and Data Type Mapping in Copy Activity

## **Recommended Steps**

* In some scenarios, _"structure"_ section in _dataset_ is required, including:
  * Applying explicit data type conversion for file sources during copy (input dataset) <br>
  * Applying explicit column mapping during copy (both input and output dataset) <br>
  * Copying from Dynamics 365/CRM source (input dataset) <br>
  * Copying to Cosmos DB as nested object when source is not JSON files (output dataset) <br>
* Please refer to [_Dataset "Structure"_](https://docs.microsoft.com/azure/data-factory/copy-activity-schema-and-type-mapping#when-to-specify-dataset-structure) section for complete list <br>
* Dataset _"structure"_ schema is specified [here](https://docs.microsoft.com/azure/data-factory/concepts-datasets-linked-services#dataset-structure) <br>

## **Recommended Documents**

Copy Activity Schema Mapping [Document](https://docs.microsoft.com/azure/data-factory/copy-activity-schema-and-type-mapping), including following sections: <br>

* [Column mapping](https://docs.microsoft.com/azure/data-factory/copy-activity-schema-and-type-mapping#column-mapping) <br>
* [Schema mapping](https://docs.microsoft.com/azure/data-factory/copy-activity-schema-and-type-mapping#schema-mapping) <br>
* [Data type mapping](https://docs.microsoft.com/azure/data-factory/copy-activity-schema-and-type-mapping#data-type-mapping) <br>
