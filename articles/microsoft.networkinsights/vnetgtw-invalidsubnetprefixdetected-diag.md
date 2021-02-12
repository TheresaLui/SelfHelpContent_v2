<properties
pageTitle="Virtual Network Gateway Has detected Invalid Subnet Prefix"
description="Virtual Network Gateway Has detected Invalid Subnet Prefix"
infoBubbleText="Issues with your Virtual Network Gateway were detected. See details on the right."
service="microsoft.network"
resource="VirtualNetworkGateway"
authors="chadmath"
displayOrder="1"
articleId="VNGTenantLogsInvalidSubnetPrefixInsight2"
diagnosticScenario="VNGTenantLogsInvalidSubnetPrefixInsight"
selfHelpType="Diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="CloudNet_AzureVPNGateway"
/>
# Invalid subnet prefixes detected
<!--issueDescription-->
We have identified your Virtual Network Gateway for Vnet, **<!--$virtualNetworkName-->[virtualNetworkName]<!--/$virtualNetworkName-->** with an IP of: **<!--$gatewayVip-->[gatewayVip]<!--/$gatewayVip-->** has an invalid prefix specified for the subnet: **<!--$subnet-->[subnet]<!--/$subnet-->**.

## **Issue Details & Mitigation**
We recommend reviewing and correcting the IP address range (prefix) for subnet: **<!--$subnet-->[subnet]<!--/$subnet-->**.

**For mission-critical workloads we recommend setting up monitoring alerts for Virtual Network Gateways. More can be read on this [here](https://docs.microsoft.com/azure/network-watcher/network-watcher-monitor-with-azure-automation)**.
