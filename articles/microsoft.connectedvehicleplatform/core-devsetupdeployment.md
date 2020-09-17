<properties
	pageTitle="Partner Kit Deployment"
	description="DevSetup deployment issues"
	service="microsoft.connectedvehicleplatform"
	resource="core"
	authors="jbeman"
	ms.author="jbeman"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32725767"
	resourceTags=""
	productPesIds="16918"
	cloudEnvironments="public"
	articleId="core-devsetup-deployment"
	ownershipId="AzureIot_Mobility"
/>

# DevSetup Install Issues

## Error: Docker version 'x.xx.x' is required

Q: When running DevSetup.ps1 step 3, in section 'Windows 10 VM Setup and Cloud Deployment', found in **Tutorial 2: Deploy the Connected Vehicle Platform**, I get an error `Docker version 'x.xx.x' is required. Installed version ''`, when running the following script `.\packages\Microsoft.Azure.ConnectedCar.Deployment.*\DevSetup.ps1`.
A: Wait until Docker has started before running DevSetup.ps1.

## Error: ‘keyvault_objectid’ is null

Q: When running DevSetup.ps1 step 3, in section **Windows 10 VM Setup and Cloud Deployment**, found in **Tutorial 2: Deploy the Connected Vehicle Platform**, the following error occurs when deploying to the KeyVault.
A: There are two possible causes:

1. This error occurs when the user has either not logged into the subscription or has logged onto multiple subscriptions.
    - Set the last parameter `-Automation $true` which will force the user to login to the subscription. We may need to clarify the following instructions that detail the `–Automation` parameter
    - Log into your subscription using the script 'Connect-AzAccount'

2. The user has two formats of the same account, e.g. first.last@company.com and firstlast@company.com
    - Contact Connected Vehicle Platform team to update account registration in Active Directory needs to be changed

## **Recommended Documents**

- [Tutorial 2: Deploy the Connected Vehicle Platform](https://dev.azure.com/mcvp-prod/Partner%20Kits/_git/mcvp-pkit?path=%2Farticles%2Fpk%2Ftutorials%2Fgeneral-audience-deployPartnerKits.md)
