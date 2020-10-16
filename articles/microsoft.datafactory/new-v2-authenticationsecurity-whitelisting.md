<properties
	pageTitle="Firewall Configurations and IP Whitelisting"
	description="For Self-hosted Integration Runtime"
	infoBubbleText=""
	authors="chez-charlie"
	ms.author="chez"
	articleId="23cf5f6a-07fc-4093-b597-ab70faf9ce37"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32629493"
	resourceTags=""
	productPesIds="15613"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_DataFactory"
/>

# IP Whitelisting and Firewall Configurations for Self-hosted Integration Runtime

## **Recommended Documents**

* Hybrid Scenarios Security [Overview](https://docs.microsoft.com/azure/data-factory/data-movement-security-considerations#hybrid-scenarios) <br>
* Firewall Configurations and Allow list IP Addresses: <br>
  * [For on-prem/private network](https://docs.microsoft.com/azure/data-factory/data-movement-security-considerations#firewall-requirements-for-on-premisesprivate-network) <br>
  * [In data store](https://docs.microsoft.com/azure/data-factory/data-movement-security-considerations#ip-configurations-and-whitelisting-in-data-stores) <br><br>


### **Note**
On October 13th 2020 some customers might have received a notification about new IP ranges being added on multiple regions as part of ADF service growth.

Starting November 8th 2020 the new IP ranges will start being used by Azure Data Factory service.<br> 
Customers that use firewall rules based on service tags or FQDNs will not have to make any updates on their configuration, if you have custom firewall **outbound rules** based on IP addresses, for existing Self-Hosted IR or SSIS IR configured before October 13th, reagrdless if they are configured on-premise or on Azure virtual private network, please review our [Troubleshooting Guide](https://docs.microsoft.com/azure/data-factory/self-hosted-integration-runtime-troubleshoot-guide#receiving-email-to-update-the-network-configuration-to-allow-communication-with-new-ip-addresses) 
