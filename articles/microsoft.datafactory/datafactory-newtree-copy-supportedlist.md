<properties
	pageTitle="V2 - Copy Activity – Connectivity"
	description="Connectivity troubleshooting"
	infoBubbleText=""
	service="microsoft.datafactory"
	resource="factories"
	authors="chez-charlie, hecepeda"
	ms.author="chez"
	displayOrder="5"
	articleId="76fb1062-d878-4507-a0d9-8e5f959c6e1b"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32629470"
	resourceTags=""
	productPesIds="15613"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_DataFactory"
/>

# V2 - Copy Activity – Connectivity

**Note -** If you use **Self-Hosted IR** please follow the steps on the [troubleshooting guide](https://docs.microsoft.com/azure/data-factory/self-hosted-integration-runtime-troubleshoot-guide#gather-self-hosted-integration-runtime-logs-from-azure-data-factory), and take note of the **Report ID** to provide it with the support request.

Many problems related with connectivity, using a **copy activity**, are related with configuration steps on how to authenticate to the source/sink data or with the permissions configured for the account accessing the data.

Depending on your scenario, the troubleshooting actions might require multiple steps.

## **Recommended Steps**

1. Obtain the error that is returned while trying to execute the pipeline or when trying to connect to the data set. You can try testing the connection by editing the linked service and pressing the button **Test connection**.
2. Review the documented common errors and solutions, you can find a great variety of errors and how to resolve them on the following troubleshooting guides:
   * [SQL connector](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide#azure-sql-data-warehouseazure-sql-databasesql-server)
   * [Azure Storage connector](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide#azure-blob-storage)
   * [ADLS Gen 1 connector](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide#azure-data-lake-storage-gen1)
   * [ADLS Gen 2 connector](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide#azure-data-lake-storage-gen2)
   * [Cosmos DB connector](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide#azure-cosmos-db)
   * [General Copy Activity errors](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide#general-copy-activity-error)
3. If you are using a self-hosted IR to connect to your data, make sure you test your connectivity from the Self-Hosted IR machine, access the **Microsoft Integration Runtime Configuration Manager**, and make sure it shows it is connected to the cloud service, then go to the **Diagnostics** tab and test the connection to your data source/sink.
4. Make sure that Networking security components such as Firewalls, Network Security Groups, VPN configurations have not changed if your scenario makes use of any of these components, you can review the [data movement security considerations](https://docs.microsoft.com/azure/data-factory/data-movement-security-considerations#firewall-configurations-and-allow-list-setting-up-for-ip-address-of-gateway) documentation to ensure all configurations are correct.
5. If after reviewing the logs and online articles related to them, you still need assistance, please continue opening a support request and make sure to mention the specific error you are obtaining and attach the logs you gathered while troubleshooting the problem.

### **Data Format Troubleshooting**

For problems with the data formats supported by the data source or sink, review the following troubleshooting guides containing common errors and solutions:
* [JSON common errors and troubleshooting](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide#json-format)
* [Parquet common errors and troubleshooting](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide#parquet-format)
* [Delimited text troubleshooting](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide#delimited-text-format)

## **Recommended Documents**

* List of [Supported Data Stores](https://docs.microsoft.com/azure/data-factory/copy-activity-overview#supported-data-stores-and-formats) <br> 
* List of [Supported File Formats and Compression Codecs](https://docs.microsoft.com/azure/data-factory/supported-file-formats-and-compression-codecs)


### **FAQ and Features request**

* [Azure Data Factory FAQ](https://docs.microsoft.com/azure/data-factory/frequently-asked-questions)
* [Feature Request](https://feedback.azure.com/forums/270578-azure-data-factory)
