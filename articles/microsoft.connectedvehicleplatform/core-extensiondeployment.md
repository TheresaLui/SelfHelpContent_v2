<properties
	pageTitle="Extension Deployment"
	description="Process extension deployment issues"
	service="microsoft.connectedvehicleplatform"
	resource="core"
	authors="gobbyo"
	ms.author="jbeman"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32725773"
	resourceTags=""
	productPesIds="16918"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="core-extension-deployment"
	ownershipId="AzureIot_Mobility"
/>

# Extension Deployment

## **Recommended Steps**

## Error: PLEASE ENSURE PLATFORM IS RUNNING

The following error occurs when attempting to deploy an extension: `PLEASE ENSURE PLATFORM IS RUNNING.  ALTHOUGH THIS PROGRAM WILL RETRY, PLATFORM MUST BE RUNNING FOR IT TO SUCCEED.`

There are two possible causes for this error:

1. Check the service fabric explorer on your cloud VM as service fabric may not be running or in an unhealthy state. Rerun steps 5 and 6 in the **Windows 10 VM Setup and Cloud Deployment** section, found in the **Tutorial: Deploy the Connected Vehicle Platform to Azure** to fix service fabric.

2. This error may have be caused by using the `VehicleProvisioningApi-Key1` instead of the `CcApiKey-Key1` from your key vault. Note that each swagger API requires a different key from your key vault, e.g. vehicle provisioning, command, resource manager. Get the `CcApiKey-Key1` by running the following script in a PowerShell session:

    `(Get-AzKeyVaultSecret -VaultName "{your key vault name}" -name "CcApiKey-Key1").SecretValueText`

    Use the secret value text for `CCApiKey-Key1` from your key vault to set the `-CVSApiKey` parameter in the `DeployProcessExtension.ps1` script. Rerun the script.

## Error: Awaiting rollout of manifest to extension host

Verify the connectivity between your machine (deploying the extension), and the cloud Azure resources. Reconnect and create a new RDP session.

## **Recommended Documents**

- [Create a Virtual Machine for the Cloud](https://dev.azure.com/mcvp-prod/Partner%20Kits/_git/mcvp-pkit?path=%2Farticles%2Fpk%2Ftutorials%2Fgeneral-audience-tutorial-prerequisites.md)
- [How to Deploy Custom Extensions](https://dev.azure.com/mcvp-prod/Partner%20Kits/_git/mcvp-pkit?path=%2Farticles%2Fpk%2Fhow-to-guides%2Fgeneral-audience-how-to-deploy-extensions.md)
- [Create a Virtual Machine for the Cloud](https://dev.azure.com/mcvp-prod/Partner%20Kits/_git/mcvp-pkit?path=%2Farticles%2Fpk%2Ftutorials%2Fgeneral-audience-tutorial-prerequisites.md)
