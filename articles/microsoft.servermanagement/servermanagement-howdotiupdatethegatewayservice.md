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

You can configure gateway updates to occur automatically or manually in the Gateway update settings. If “Automatic” is selected, the update will be installed within 24 hours after the update has become available. If “Manual” is selected, you will need to choose “Schedule now” to schedule a one-time update to occur within the next 24 hours. If an immediate update is necessary, you will need to reinstall a new gateway deployment package. Log on to the gateway machine, go to “Programs and Features” and uninstall “Server management tools gateway”. Then, generate a new gateway deployment package, download and install it on the gateway machine.

