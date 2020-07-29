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
/>

# How to check sync feature state 

* Check the Password Hash Sync feature state in Azure AD. 
* You can do that by using the cmdlet on the AADConnect server

~~~powershell

Get-ADSyncAADCompanyFeature -ConnectorName 'case sensitive AAD Connector name'

~~~


