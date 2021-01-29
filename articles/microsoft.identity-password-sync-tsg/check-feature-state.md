<properties
	pageTitle="Check sync feature state"
	description="Check sync feature state"
	service="microsoft.identity"
	resource=""
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="894f3a14-8b55-46df-9ef0-c374b6b4e40d"
	   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# How to check sync feature state 

1. Check the Password Hash Sync feature state in Azure AD. 
2. You can do that by using the cmdlet on the AADConnect server

~~~powershell

Get-ADSyncAADCompanyFeature -ConnectorName 'case sensitive AAD Connector name'

~~~


