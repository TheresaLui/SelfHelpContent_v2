<properties
	pageTitle="Send Command"
	description="Issues when sending a command"
	service="microsoft.connectedvehicleplatform"
	resource="core"
	authors="gobbyo"
	ms.author="jbeman"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32725756"
	resourceTags=""
	productPesIds="16918"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="core-sendcommand"
	ownershipId="AzureIot_Mobility"
/>

# Send Command

## Error: BadRequest

When using the command line application to send a command from the tutorial to **Send, Receive, and Respond to a Command**, the status code resulted in a `BadRequest`.

## **Recommended Steps**

The most common reasons for this error:

1. Incorrect vehicle or device name in the Command Extension

    - Repeat step 2 from the **Tutorial: Send, Receive, and Respond to a Command**, verify and change your vehicle or device name, then redeploy your command custom extension.

2. Missing claims for the vehicle

    - Add the missing claim for the vehicle.  Follow the instructions to **Create Claims for Vehicle Telemetry** found in the **Tutorial: Deploy the Sample Claims Application and Create Claims**.  Then rerun the section **Send a Command** in the **Tutorial: Send, Receive, and Respond to a Command**.

## **Recommended Documents**

- [Tutorial: Send, Receive, and Respond to a Command](https://dev.azure.com/mcvp-prod/Connected%20Vehicle%20Platform/_git/mcvp-prod?path=%2Farticles%2Fpk%2Ftutorials%2Fgeneral-audience-command-tutorial.md)
- [Tutorial: Deploy the Sample Claims Application and Create Claims](https://dev.azure.com/mcvp-prod/Partner%20Kits/_git/mcvp-pkit?path=%2Farticles%2Fpk%2Ftutorials%2Fgeneral-audience-create-a-claim-tutorial.md)
- [How to Deploy Custom Extensions](https://dev.azure.com/mcvp-prod/Partner%20Kits/_git/mcvp-pkit?path=%2Farticles%2Fpk%2Fhow-to-guides%2Fgeneral-audience-how-to-deploy-extensions.md)
