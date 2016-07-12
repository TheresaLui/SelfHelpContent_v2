<properties
	pageTitle="How do I update the gateway service?"
	description="How do I update the Server management tools gateway service?"
	service="microsoft.servermanagement"
	resource="gateways"
	authors="jol"
	displayOrder="4"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>

# How do I update the gateway service?
* You can configure gateway updates to occur automatically or manually in the Gateway update settings. If “Automatic” is selected, the update will be installed within 30 minutes after the update has become available. If “Manual” is selected, you will need to choose “Schedule now” to schedule a one-time update to occur within the next 30 minutes. 
* If an immediate update is necessary, you can do so by restarting the gateway service. Log on to the gateway machine, go to Task Manager or Services MMC snap-in and restart the "ServerManagementToolsGateway" service.

