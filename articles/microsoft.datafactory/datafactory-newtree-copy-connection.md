<properties
  pagetitle="Troubleshooting Guidance "
  description="Connect to Data Store"
  service="microsoft.datafactory"
  resource="factories"
  ms.author="chez,brianwan"
  selfhelptype="Generic"
  supporttopicids="32629463"
  resourcetags=""
  productpesids="15613"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="bb90be20-446f-4995-91f4-f9e62808ea7f"
  ownershipid="AzureData_DataFactory" />
# Troubleshooting Guidance 

Troubleshoot many common issues in Azure Data Factory using this article.

**Note:** If you use Self-Hosted integration runtime (IR), follow the steps in the [troubleshooting guide](https://docs.microsoft.com/azure/data-factory/self-hosted-integration-runtime-troubleshoot-guide#gather-self-hosted-integration-runtime-logs-from-azure-data-factory), and take note of the **Report ID** to provide it with the support request.

If you encounter unexpected error from source or sink side such as ParquetJavaInvocationException, review [Troubleshoot Azure Data Factory Connectors](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide) for most known issues.

If you encounter unexpected error during the copy activity, review [Connector and copy activity](https://docs.microsoft.com/azure/data-factory/data-factory-troubleshoot-guide#connector-and-copy-activity) for most known issues.

## **Recommended Steps** 

* For a Linked Service configuration guide, review [Data Store connectors](https://docs.microsoft.com/azure/data-factory/copy-activity-overview#supported-data-stores-and-formats) 
* For on-prem network, make sure to allow list the following [IP addresses](https://docs.microsoft.com/azure/data-factory/data-movement-security-considerations#firewall-configurations-and-whitelisting-ip-address-of-gateway)

## **Recommended Documents**

* List of [Supported data stores](https://docs.microsoft.com/azure/data-factory/copy-activity-overview#supported-data-stores-and-formats)
* [Firewall configurations and allow listing IP Addresses](https://docs.microsoft.com/azure/data-factory/data-movement-security-considerations#firewall-configurations-and-whitelisting-ip-address-of-gateway)
* [Self-Hosted IR troubleshooting guide](https://docs.microsoft.com/azure/data-factory/self-hosted-integration-runtime-troubleshoot-guide)
* [Troubleshoot Azure Data Factory connectors](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide)
* [Connector and copy activity](https://docs.microsoft.com/azure/data-factory/data-factory-troubleshoot-guide#connector-and-copy-activity)
