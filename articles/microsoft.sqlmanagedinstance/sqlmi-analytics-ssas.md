<properties
	pageTitle="Reporting Analytics Integration|SSAS"
	description="Reporting Analytics Integration|SSAS"
	service="microsoft.sql"
	resource="servers"
	authors="MladjoA"
    ms.author="mlandzic"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32637231"
	productPesIds="16259"
	cloudEnvironments="public"
/>

# SSAS and Azure Analysis Services

Azure SQL Managed Instance is a cloud service injected into customer's VNet and by default not available from the Azure Analysis Services (AAS).
Optional public endpoint of managed instance is still not consumable from AAS.

## **Recommended steps**

- Use [on-premises data gateway](https://docs.microsoft.com/power-bi/service-gateway-onprem) to reach VNet-injected managed instance from AAS