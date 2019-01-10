<properties
	pageTitle="Failed to process model with data source through gateway"
	description="Failed to process model with data source through gateway"
	service="microsoft.analysisservices"
	resource="servers"
	authors="bnmaa"
	displayOrder="3"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="MoonCake"
/>

# Failed to process model with data source through gateway

## **Recommended steps**

1. Open the config file **Microsoft.PowerBI.DataMovement.Pipeline.GatewayCore.dll.config** under the installation directory of the unified gateway, typically it's **%systemdrive%\Program Files\On-premises data gateway**.
2. Find the **SendTelemetry** setting in the config, change the value to **False**.
3. Restart the gateway service **On-premise data gateway service**.
4. If processing continues to fail, follow **My issue is not listed**.
