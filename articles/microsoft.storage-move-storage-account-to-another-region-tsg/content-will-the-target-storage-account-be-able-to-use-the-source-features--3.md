<properties
	pageTitle="Check if subscription is whitelisted for preview features"
	description="Check if subscription is whitelisted for preview features"
	service=""
	resource=""
	authors="rimayber"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="a91cde02-6e44-4756-80d8-beceb5ecc30f"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Check if subscription is whitelisted for preview features

Source storage account has preview features. We should check the preview features documentation on how to request enabling this feature on the subscription in the target region. Usually, following are the common different ways a preview feature can be requested to enable. 

1. Using a powershell script. Following is an example. Each feature might have a different or similar syntax.

~~~powershell

   Register-AzProviderFeature -FeatureName BlobIndex -ProviderNamespace Microsoft.Storage

~~~

2. Using a CLI Command.

~~~console

az feature register --namespace Microsoft.Storage --name BlobIndex

~~~

3. Filling an online form.
4. Emailing to a special feature email account.
5. Creating an Support Request to XEEE via ICM.
