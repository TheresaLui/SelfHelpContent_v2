<properties
	pageTitle="On-premises data gateway is not working"
	description="On-premises data gateway is not working"
	service="microsoft.analysisservices"
	resource="servers"
	authors="bnmaa"
	displayOrder="4"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="MoonCake"
/>

# On-premises data gateway is not working

While processing, if there's an error like `Gateway on endpoint '<endpoint uri>' is unreachable`, make sure the gateway is configured correctly and it's the gateway associated with the AS server.

## **Recommended steps**

1. Open **On-premises data gateway** in the on-premises server and sign in, check the name and the region, and make sure the network status is **Connected**.
2. Open **System Information** in the on-premises server and check the System Name(hostname).
3. Browse **On-premises Data Gateway** blade of the AS server in Azure portal, make sure that **AS Region** is same as the region configured in **On-premises data gateway**.
4. Browse overview blade of the **On-premises Data Gateway** associated with the AS server, make sure that **Machine name** is same as the on-premises server.

## **Recommended documents**
[Connecting to on-premises data sources with Azure On-premises Data Gateway](https://docs.microsoft.com/azure/analysis-services/analysis-services-gateway)
