<properties
  pagetitle="Troubleshooting Guidance "
  description="Connect to Data Store"
  service="microsoft.datafactory"
  resource="factories"
  ms.author="yingu"
  selfhelptype="Generic"
  supporttopicids="32629463"
  resourcetags=""
  productpesids="15613"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="bb90be20-446f-4995-91f4-f9e62808ea7f"
  ownershipid="AzureData_DataFactory" />
# Troubleshooting Guidance 

You can resolve many common issues in Azure Data Factory using the following information.

## Troubleshoot common connectivity issues

- **Connectivity issues between Self-Hosted IR and Source/Sink**
 
    * If a corporate firewall runs on the central router of the organization, review [the outbound port and domain requirements for corporate firewalls](https://docs.microsoft.com/azure/data-factory/data-movement-security-considerations?WT.mc_id=Portal-Microsoft_Azure_Support#firewall-requirements-for-on-premisesprivate-network).
    * If the issue persists, use a Netmon trace to further analyze the issue. Follow the steps in the [Network troubleshooting guide](https://docs.microsoft.com/azure/data-factory/self-hosted-integration-runtime-troubleshoot-guide?WT.mc_id=Portal-Microsoft_Azure_Support#connectivity-issue-between-self-hosted-ir-and-data-factory-or-self-hosted-ir-and-data-sourcesink).

- **Connectivity issues between Azure IR and Source/Sink**

    * If Managed Virtual Network is enabled, check the [Limitations and known issues](https://docs.microsoft.com/azure/data-factory/managed-virtual-network-private-endpoint#limitations-and-known-issues). For more information, see [Managed Virtual Network](https://docs.microsoft.com/azure/data-factory/managed-virtual-network-private-endpoint#managed-virtual-network).
    * If your data store has firewall settings, allow traffic from the IP addresses listed for the Azure Integration runtime in the specific Azure region. You can get an IP range list of service tags from the [service tags IP range download link](https://docs.microsoft.com/azure/virtual-network/service-tags-overview?WT.mc_id=Portal-Microsoft_Azure_Support#discover-service-tags-by-using-downloadable-json-files). For example, if the Azure region is AustraliaEast, get an IP range list from DataFactory.AustraliaEast.

## Troubleshoot connector specific issues

* If you encounter unexpected error from source or sink side, see [Troubleshoot Azure Data Factory Connectors](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide?WT.mc_id=Portal-Microsoft_Azure_Support) for most known issues.

* For more information, see the specific connector’s document at [Data Store connectors](https://docs.microsoft.com/azure/data-factory/copy-activity-overview?WT.mc_id=Portal-Microsoft_Azure_Support#supported-data-stores-and-formats).
    * For example, if you're using Polybase to load data into Azure Synapse Analytics, see [Azure Synapse Analytics](https://docs.microsoft.com/azure/data-factory/connector-azure-sql-data-warehouse#use-polybase-to-load-data-into-azure-synapse-analytics) for known issues and best practices.

## **Recommended Documents**

* [List of supported data stores](https://docs.microsoft.com/azure/data-factory/copy-activity-overview#supported-data-stores-and-formats)
* [Firewall configurations and allow listing IP Addresses](https://docs.microsoft.com/azure/data-factory/data-movement-security-considerations#firewall-configurations-and-whitelisting-ip-address-of-gateway)
* [Self-hosted IR troubleshooting guide](https://docs.microsoft.com/azure/data-factory/self-hosted-integration-runtime-troubleshoot-guide)
* [Troubleshoot Azure Data Factory connectors](https://docs.microsoft.com/azure/data-factory/connector-troubleshoot-guide)
* [Connector and copy activity](https://docs.microsoft.com/azure/data-factory/data-factory-troubleshoot-guide#connector-and-copy-activity)

**Note:** If you use self-hosted integration runtime (IR), follow the steps in the [troubleshooting guide](https://docs.microsoft.com/azure/data-factory/self-hosted-integration-runtime-troubleshoot-guide#gather-self-hosted-integration-runtime-logs-from-azure-data-factory), and take note of the **Report ID** so that you can provide it with the support request.
