<properties
	pageTitle="Check Brooklyn Diagnostic Logs for Route Based VPN"
	description="Check Brooklyn Diagnostic Logs for Route Based VPN"
	service="microsoft.network"
	resource="vpnGateways"
	authors="riturajc"
	ms.author="arshads, riturajc, shshrao"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds="32591158,32584882,32584881"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="477a5749-9a75-440e-8f9f-fe4b536b45bf"
	ownershipId="CloudNet_AzureVPNGateway"
/>

# Host Maintenance - RCA

## **Recommended Steps**

*I would like to inform you that there are no notifications triggered to any customers when there is any upgrade \ host maintenance activity occurs on the VPN Gateway as this covers within the SLA. VPN Gateway in Azure consists of 2 Tenants i.e., Primary and Secondary Instances. During internal maintenance \ upgrade a failover gets triggered which failover where the Primary Instance hands off the config to the secondary which becomes active and after the upgrade is complete the secondary instance goes through an internal maintenance \ upgrades which triggers another failover handing over the configuration to Primary instance.*

*While I understand that this impacted your business and for which I would like to apologize however to avoid such events we recommend that you setup High Availability VPN setup where both the instances of the gateway are always active and even if one of the gateway undergoes an update the impact is very limited.*

## **Recommended Documents**