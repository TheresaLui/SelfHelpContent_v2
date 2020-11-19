<properties
	pageTitle="Partner Kit Deployment"
	description="DevSetup deployment issues"
	service="microsoft.connectedvehicleplatform"
	resource="core"
	authors="gobbyo"
	ms.author="jbeman"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32725767"
	resourceTags=""
	productPesIds="16918"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="core-devsetup-deployment"
	ownershipId="AzureIot_Mobility"
/>

# DevSetup Install Issues

## Error: Docker version 'x.xx.x' is required

Q: When running `DevSetup.ps1` in step 3, from the section **Windows 10 VM Setup and Cloud Deployment**, found in **Tutorial 2: Deploy the Connected Vehicle Platform**, I get an error `Docker version 'x.xx.x' is required. Installed version ''`, when running the following script `.\packages\Microsoft.Azure.ConnectedCar.Deployment.*\DevSetup.ps1`.

A: Wait until Docker has started then rerun the `DevSetup.ps1` script.

## Error: ‘keyvault_objectid’ is null

When running `DevSetup.ps1` in step 3, section **Windows 10 VM Setup and Cloud Deployment**, found in **Tutorial 2: Deploy the Connected Vehicle Platform**, the error `‘keyvault_objectid’ is null` occurs when deploying to the KeyVault.

## **Recommended Steps**

There are two possible causes for the error `‘keyvault_objectid’ is null`:

1. When you have logged into the subscription or you have logged into multiple subscriptions.
    - Before running the `DevSetup.ps1` script, set the last parameter as  `-Automation $true` which will force you to login to your subscription
    - Log into your subscription using the script 'Connect-AzAccount -TenantId {your tenantID} -SubscriptionId {your subscription}' before running `DevSetup.ps1`

2. When you have two formats of the same account, e.g. first.last@company.com and firstlast@company.com
    - Contact the Connected Vehicle Platform team to update your account registration in Active Directory

## **Recommended Documents**

- [Tutorial 2: Deploy the Connected Vehicle Platform](https://dev.azure.com/mcvp-prod/Partner%20Kits/_git/mcvp-pkit?path=%2Farticles%2Fpk%2Ftutorials%2Fgeneral-audience-deployPartnerKits.md)
