<properties
  pagetitle="IP allow listing and firewall configurations for self-hosted integration runtime (SHIR)"
  ms.author="chez,lle,susabat"
  selfhelptype="Generic"
  supporttopicids="32629493"
  resourcetags=""
  productpesids="15613"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="23cf5f6a-07fc-4093-b597-ab70faf9ce37"
  ownershipid="AzureData_DataFactory" />
# IP allow listing and firewall configurations for self-hosted integration runtime (SHIR)

* On December 8, 2020, some customers received notification about adding new IP addresses of Azure Integration Runtime in the specific Azure region. Starting January 15, 2021, these IP addresses will be available for use by Azure Integration Runtime.<br>

   These new IP addresses will have no impact and require no action for customers who:
   * Have no inbound blocking rules in resources that only allow IP addresses of Azure Integration Runtime in specific Azure Region
   * Use service tags in these blocking rules 

   To learn more, please see [Data Access Strategies](https://docs.microsoft.com/azure/data-factory/data-access-strategies) and  [Configure Azure Integration Runtime IP addresses](https://docs.microsoft.com/azure/data-factory/azure-integration-runtime-ip-addresses)

* On October 13, 2020, some customers received notification that new IP ranges were added on multiple regions as part of ADF service growth. Starting November 8, 2020, Azure Data Factory service began using these IP ranges.

   * Customers who use firewall rules based on service tags or FQDNs will not have to update their configuration if they have custom firewall **outbound rules** that are based on IP addresses.

   * If you have a Self-Hosted IR or an SSIS IR configured before October 13, 2020 and configured on-premise or on an Azure virtual private network, please make sure to review our [Troubleshooting Guide](https://docs.microsoft.com/azure/data-factory/self-hosted-integration-runtime-troubleshoot-guide#receiving-email-to-update-the-network-configuration-to-allow-communication-with-new-ip-addresses).

## **Recommended Documents**

* Hybrid Scenarios Security [Overview](https://docs.microsoft.com/azure/data-factory/data-movement-security-considerations#hybrid-scenarios) 
* Firewall Configurations and Allow list IP Addresses: 
  * [For on-prem/private network](https://docs.microsoft.com/azure/data-factory/data-movement-security-considerations#firewall-requirements-for-on-premisesprivate-network) 
  * [In data store](https://docs.microsoft.com/azure/data-factory/data-movement-security-considerations#ip-configurations-and-whitelisting-in-data-stores) 
* [Azure Data Factory Supports Static IP Addresses for Data Movement, Pipelines and Actvities](https://techcommunity.microsoft.com/t5/azure-data-factory/azure-data-factory-now-supports-static-ip-address-ranges/ba-p/1117508)