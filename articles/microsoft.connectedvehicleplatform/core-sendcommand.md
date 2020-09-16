<properties
	pageTitle="Send Command"
	description="Issues when sending a command"
	service="microsoft.connectedvehicleplatform"
	resource="core"
	authors="jbeman"
	ms.author="jbeman"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32725756"
	resourceTags=""
	productPesIds="16918"
	cloudEnvironments="public"
	articleId="core-sendcommand"
	ownershipId="AzureIot_Mobility"
/>

# Send Command

## Error: BadRequest

Q: When following the Send a Command instructions found in the **Tutorial: Send, Receive, and Respond to a Command**, the status code resulted in a `BadRequest`
A: There are a number of reasons this error may occur—the most common are the following:

1. Incorrect vehicle or device name in the Command Extension

- Repeat step 2 from the **Tutorial: Send, Receive, and Respond to a Command** and redeploy your command extension.

2. Missing claims for the vehicle

- Add the missing claim for the vehicle.  Follow the instructions to **Create Claims for Vehicle Telemetry** found in the **Tutorial: Deploy the Sample Claims Application and Create Claims**.  Then rerun the section **Send a Command** in the **Tutorial: Send, Receive, and Respond to a Command**.

## **Recommended Documents**

- https://dev.azure.com/mcvp-prod/Connected%20Vehicle%20Platform/_git/mcvp-prod?path=%2Farticles%2Fpk%2Ftutorials%2Fgeneral-audience-command-tutorial.md&version=GBrelease%2Fvnext%2Fmcvp.2.3.700-pre.100&createIfNew=true
- https://dev.azure.com/mcvp-prod/Partner%20Kits/_git/mcvp-pkit?path=%2Farticles%2Fpk%2Fhow-to-guides%2Fgeneral-audience-how-to-deploy-extensions.md&version=GBrelease%2Fvnext%2Fmcvp.2.10.800&_a=preview