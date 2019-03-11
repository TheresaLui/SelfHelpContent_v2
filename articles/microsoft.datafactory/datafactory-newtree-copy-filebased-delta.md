<properties
	pageTitle="Delta Load from File Based Storage"
	description="Only copy new or modified files after certain date"
	infoBubbleText=""
	authors="chez-charlie"
	ms.author="chez"
	articleId="ae9dc41f-5b58-4a01-98bb-db9594133eb4"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32629456"
	resourceTags=""
	productPesIds="15613"
	cloudEnvironments="public"
/>

# Incremental Copy from File Based Storage

Note: this is a _new feature_ of Azure Data Factory.

## **Recommended Steps**

You can incrementally copy new or updated files, by filtering on their __LastModifiedDate__ attribute. Currently, this feature is available when copy from following connectors: <br>

* Azure Blob Storage
* Amazon S3
* File System

New feature supported in

* ADF Portal: for dataset, in _Connection_ section, specify _Start time_ and _End time_ for _Filter by last modified_
* Copy Data Tool: set the file loading behavior to _Incremental load: LastModifiedDate_
* SDK: specify dataset properties _modifiedDatetimeStart_ and _modifiedDatetimeEnd_

## **Recommended Documents**

* Azure Blob Storage: [Document](https://docs.microsoft.com/azure/data-factory/connector-azure-blob-storage) <br>
* Amazon S3: [Document](https://docs.microsoft.com/azure/data-factory/connector-amazon-simple-storage-service) <br>
* File System: [Document](https://docs.microsoft.com/azure/data-factory/connector-file-system) <br>
