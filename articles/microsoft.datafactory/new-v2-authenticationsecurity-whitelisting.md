<properties
  pagetitle="IP Whitelisting and Firewall Configurations for Self-hosted Integration Runtime&#xD;"
  ms.author="chez,lle"
  selfhelptype="Generic"
  supporttopicids="32629493"
  resourcetags=""
  productpesids="15613"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="23cf5f6a-07fc-4093-b597-ab70faf9ce37"
  ownershipid="AzureData_DataFactory" />
# IP Whitelisting and Firewall Configurations for Self-hosted Integration Runtime

## **Recommended Documents**

* Hybrid Scenarios Security [Overview](https://docs.microsoft.com/azure/data-factory/data-movement-security-considerations#hybrid-scenarios) <br>
* Firewall Configurations and Allow list IP Addresses: <br>
  * [For on-prem/private network](https://docs.microsoft.com/azure/data-factory/data-movement-security-considerations#firewall-requirements-for-on-premisesprivate-network) <br>
  * [In data store](https://docs.microsoft.com/azure/data-factory/data-movement-security-considerations#ip-configurations-and-whitelisting-in-data-stores) <br><br>


### **Note**

1. 
On December 8th 2020 some customers might have received a notification about adding new IP addresses of Azure Integration Runtime in the specific Azure region.

Starting January 15th 2021 the new IP addresses will start being used by Azure Integration Runtime.<br>

If customers don't have any inbound blocking rules in resources that only allow IP addresses of Azure Integration Runtime in specific Azure Region or customers use service tag in these blocking rules, then the new IP addresses have no impact on their businesses, and they don’t need to take any actions.

You can learn more about how to configure Azure Integration Runtime IP addresses from [more details](https://docs.microsoft.com/azure/data-factory/azure-integration-runtime-ip-addresses).

2. 

On October 13th 2020 some customers might have received a notification about new IP ranges being added on multiple regions as part of ADF service growth.

Starting November 8th 2020 the new IP ranges will start being used by Azure Data Factory service.<br> 

Customers that use firewall rules based on service tags or FQDNs will not have to make any updates on their configuration, if you have custom firewall **outbound rules** based on IP addresses, for existing Self-Hosted IR or SSIS IR configured before October 13th, regardless if they are configured on-premise or on Azure virtual private network, please review our [Troubleshooting Guide](https://docs.microsoft.com/azure/data-factory/self-hosted-integration-runtime-troubleshoot-guide#receiving-email-to-update-the-network-configuration-to-allow-communication-with-new-ip-addresses).