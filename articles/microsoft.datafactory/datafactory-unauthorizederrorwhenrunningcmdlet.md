<properties 
	pageTitle="Unauthorized error when running a cmdlet" 
	description="I receive an unauthorized error message when running a cmdlet." 
	service="microsoft.datafactory" 
    resource="datafactories,factories"
    authors="spelluru"
    displayOrder="7"
    selfHelpType="resource"
    cloudEnvironments="public"
    supportTopicIds="32592907"
    productPesIds="15613"
    resourceTags=""
/>

# Unauthorized error when running a cmdlet

## **Recommended steps**
You may not be using the right Azure account or subscription with the Azure PowerShell. Use the following cmdlets to select the right Azure account and subscription to use with the Azure PowerShell. 

1. **Login-AzureRmAccount** - Use the right user ID and password
2. **Get-AzureRmSubscription** - View all the subscriptions for the account. 
3. **Select-AzureRmSubscription** - Select the right subscription. Use the same one you use to create a data factory on the Azure Portal.