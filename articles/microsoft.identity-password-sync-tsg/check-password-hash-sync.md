<properties
	pageTitle="Check if Password Hash Sync enabled for this forest"
	description="Check if Password Hash Sync enabled for this forest"
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
	articleId="bfa5be87-e803-4e25-a7e3-9c0807af2c65"
	   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# How to check if Password Hash Sync enabled for this forest

* If Password Hash Sync is not enabled for the forest, Password Hash Sync will not work
* To find if Password Hash Sync is enabled for the forest, run this cmdlet on the AADConnect server: 
* To learn how to enable Password Hash Sync for the forest, please read the information in the link below

~~~powershell

'Get-ADSyncAADPasswordSyncConfiguration -SourceConnector $case sensitive AD Connector name$'

~~~

## **Recommended Documents**

* [Enable password hash sync](https://docs.microsoft.com/azure/active-directory-domain-services/tutorial-configure-password-hash-sync#enable-synchronization-of-password-hashes)
