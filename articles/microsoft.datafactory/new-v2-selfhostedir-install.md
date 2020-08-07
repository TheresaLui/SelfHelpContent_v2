<properties
	pageTitle="Integration Runtime Express Setup Issue"
	description="Cannot Run Express Setup for Self-hosted IR"
	infoBubbleText=""
	authors="chez-charlie"
	ms.author="chez"
	articleId="e8457178-4061-4b46-b49d-dbdfba49afc4"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32629536"
	resourceTags=""
	productPesIds="15613"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_DataFactory"
/>

# Integration Runtime Express Setup Issue

## **Recommended Steps**

* The **Express setup** for the Integration Runtime requires Edge or another **Microsoft ClickOnce compatible web browser**. If the Express Setup fails to start, please consider the following steps: <br>

  * Please use Edge or a Microsoft ClickOnce compatible web browser <br>
  * If you are using Chrome, go to the [Chrome web store](https://chrome.google.com/webstore/), search with __"ClickOnce"__ keyword, choose one of the ClickOnce extensions, and install it <br>
  * Use the _Manual Setup_ link shown on the same pane in the UI to download the installation file and run it manually. After the installation is successful, you will see the Integration Runtime Configuration dialog box. Copy the **key** from the portal screen and use it in the configuration manager to manually register the gateway with the service.<br>

### **Common errors and solutions**
  
* **Integration Runtime registration error**: After changing the _service account_ in the Service Panel, you may find that the Integration Runtime stops working. Follow the steps mentioned in this [self-hosted IR Troubleshooting Guide](https://docs.microsoft.com/azure/data-factory/self-hosted-integration-runtime-troubleshoot-guide#self-hosted-ir-setup) to troubleshoot and resolve this error.
  
* **Integration Runtime (Self-Hosted) Node is not registered** - The __Register__ button could not be found on the Configuration Manager UI when registering a Self-hosted IR.
  * Since the release of the Integration Runtime 3.0, the **Register button on an existing Integration Runtime Node has been removed to enable a cleaner and more secure environment. If a node has been registered to some Integration Runtime (whether online or not), to re-register it to another Integration Runtime, you must uninstall the previous node, and then install and register the node.<br>
  * Follow the steps on section [cannot find register button to register self-hosted IR](https://docs.microsoft.com/azure/data-factory/self-hosted-integration-runtime-troubleshoot-guide#cannot-find-register-button-to-register-a-self-hosted-ir)<br>
  
* Unable to **register** the Self-hosted IR due to **localhost**<br>
  * When trying to register the Self-hosted IR on a new Machine, a step gives the following error message: _A runtime error has occurred. The type initializer for 'Microsoft.DataTransfer.DIAgentHost.DataSourceCache' threw an exception. A non-recoverable error occurred during a database lookup._ <br>
  * Use Localhost 127.0.0.1 on host file and resolve such issue <br>
  
* **Firewall and proxy related issues**: [possible symptoms and error messages](https://docs.microsoft.com/azure/data-factory/create-self-hosted-integration-runtime#possible-symptoms-for-firewall-and-proxy-server-related-issues) <br>
  * Please ensure **ports** are white listed for both central _corporate_ firewall and local machine _Windows_ firewall. For more details, see [Firewall Whitelisting](https://docs.microsoft.com/azure/data-factory/create-self-hosted-integration-runtime#ports-and-firewall).
  * If your IR uses proxy server, please refer to [Proxy Server](https://docs.microsoft.com/azure/data-factory/create-self-hosted-integration-runtime#proxy-server-considerations) <br>
  
 

## **Recommended Documents**

* Troubleshooting guide [Self-hosted IR setup](https://docs.microsoft.com/azure/data-factory/self-hosted-integration-runtime-troubleshoot-guide#self-hosted-ir-setup)
* How to create and configure Self-hosted Integration Runtime [Document](https://docs.microsoft.com/azure/data-factory/create-self-hosted-integration-runtime/), including: <br>
  * [Best Practice](https://docs.microsoft.com/azure/data-factory/create-self-hosted-integration-runtime#installation-best-practices) <br>
  * [Ports and Firewall](https://docs.microsoft.com/azure/data-factory/create-self-hosted-integration-runtime#ports-and-firewall) <br>
  * [Proxy Server](https://docs.microsoft.com/azure/data-factory/create-self-hosted-integration-runtime#proxy-server-considerations) <br>
* [Self-hosted integration runtime](https://docs.microsoft.com/azure/data-factory/concepts-integration-runtime#self-hosted-integration-runtime)<br>
* [Monitor integration runtime](https://docs.microsoft.com/azure/data-factory/monitor-integration-runtime/) <br>
* [Troubleshoot Self-Hosted Integration Runtime](https://docs.microsoft.com/azure/data-factory/self-hosted-integration-runtime-troubleshoot-guide) <br>
  **Note:** Please follow the steps on the [troubleshooting guide](https://docs.microsoft.com/azure/data-factory/self-hosted-integration-runtime-troubleshoot-guide#gather-self-hosted-integration-runtime-logs-from-azure-data-factory), and take note of the **Report ID** to provide it with the support request if needed.<br>
* Latest version of Self-hosted Integration Runtime [Download Page](https://www.microsoft.com/download/details.aspx?id=39717)
  * __Note__: Please refer to _Release Notes_ for feature enhancements, new capabilities, and changes introduced in the latest versions.<br>

