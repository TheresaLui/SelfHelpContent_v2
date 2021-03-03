<properties
	pageTitle="Use self-hosted IR to connect to On-prem Data Store"
	description="Integration Runtime fails to copy data to/from an on-premises data store"
	infoBubbleText=""
	authors="chez-charlie"
	ms.author="chez"
	articleId="5c190125-b0df-4fc9-a5cd-bed5004cfcd6"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32629537"
	resourceTags=""
	productPesIds="15613"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_DataFactory"
/>

# Self-Hosted Integration Runtime fails to copy data to/from an on-premises data store

**Note:** Please follow the steps on the [troubleshooting guide](https://docs.microsoft.com/azure/data-factory/self-hosted-integration-runtime-troubleshoot-guide#gather-self-hosted-integration-runtime-logs-from-azure-data-factory), and take note of the **Report ID** to provide it with the support request.

## **Recommended Steps**

* You can find detailed information in Integration Runtime logs in Windows event logs. You can find them under **Event Viewer** > **Application and Services Logs** > **Microsoft Integration Runtime**. To troubleshoot IR related issues，please look for error level events in the event viewer.
* If you see data store connection or driver related errors, launch Configuration Manager on the host machine, switch to the **Diagnostics** tab, select/enter appropriate values for fields in the **Test connection** group, and click **Test** to see if you can connect to on-premises data source from the gateway machine using the connection information and credentials <br>
* If you recently installed a driver, please restart the IR for it to pick up the latest changes <br>
* Firewall and proxy related issues: [possible symptoms and error messages](https://docs.microsoft.com/azure/data-factory/create-self-hosted-integration-runtime#possible-symptoms-for-firewall-and-proxy-server-related-issues) <br>
  * Please ensure ports are white listed for both central _corporate_ firewall and local machine _Windows_ firewall. For more details, see [Firewall Whitelisting](https://docs.microsoft.com/azure/data-factory/create-self-hosted-integration-runtime#ports-and-firewall).
  * If your IR uses proxy server, please refer to [Proxy Server](https://docs.microsoft.com/azure/data-factory/create-self-hosted-integration-runtime#proxy-server-considerations) <br>
* Try the [Troubleshooting connectivity issue](https://docs.microsoft.com/azure/data-factory/self-hosted-integration-runtime-troubleshoot-guide#troubleshoot-connectivity-issue) guidance for other errors and troubleshooting steps <br>

## **Recommended Documents**

* [Troubleshoot Self-Hosted Integration Runtime](https://docs.microsoft.com/azure/data-factory/self-hosted-integration-runtime-troubleshoot-guide) <br>
* [How to create and configure Self-hosted Integration Runtime](https://docs.microsoft.com/azure/data-factory/create-self-hosted-integration-runtime/), including: <br>
  * [Best Practice](https://docs.microsoft.com/azure/data-factory/create-self-hosted-integration-runtime#installation-best-practices) <br>
  * [Ports and Firewall](https://docs.microsoft.com/azure/data-factory/create-self-hosted-integration-runtime#ports-and-firewall) <br>
  * [Proxy Server](https://docs.microsoft.com/azure/data-factory/create-self-hosted-integration-runtime#proxy-server-considerations) <br>
* [Self-hosted integration runtime](https://docs.microsoft.com/azure/data-factory/concepts-integration-runtime#self-hosted-integration-runtime)<br>
* [Monitor integration runtime](https://docs.microsoft.com/azure/data-factory/monitor-integration-runtime/) <br>
