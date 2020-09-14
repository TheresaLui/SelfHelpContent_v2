<properties
	pageTitle="Extension Deployment"
	description="Process extension deployment issues"
	service="microsoft.connectedvehicleplatform"
	resource="core"
	authors="jbeman"
	ms.author="jbeman"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32725770,32725767"
	resourceTags=""
	productPesIds="16918"
	cloudEnvironments="public"
	articleId="core-extension-deployment"
	ownershipId="AzureIot_Mobility"
/>

# Extension Deployment

## Error: PLEASE ENSURE PLATFORM IS RUNNING

Q: The following error occurs when attempting to deploy an extension: "PLEASE ENSURE PLATFORM IS RUNNING.  ALTHOUGH THIS PROGRAM WILL RETRY, PLATFORM MUST BE RUNNING FOR IT TO SUCCEED."
A: Check your service fabric explorer as it is likely service fabric may not be running or in an unhealthy state. To fix it, rerun steps 5 and 6 in the “Windows 10 VM Setup and Cloud Deployment” section, found in the "Tutorial: Deploy the Connected Vehicle Platform to Azure."

## Error: Awaiting rollout of manifest to extension host

Q: Verify the connectivity between your machine (deploying the extension), typically a laptop, and the cloud Azure resources.
A: Reconnect your network and establish a new VPN session.

## **Recommended Documents**

- https://dev.azure.com/mcvp-prod/Partner%20Kits/_git/mcvp-pkit?path=%2Farticles%2Fpk%2Fhow-to-guides%2Fgeneral-audience-how-to-deploy-extensions.md&version=GBrelease%2Fvnext%2Fmcvp.2.10.800&_a=preview