<properties
	pageTitle="Check for agent installation errors"
	description="Check for agent installation errors"
	service="microsoft.storage"
	resource="storageAccounts"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds="32675708"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="e0cca672-4fc0-4156-8a25-9c3b512be18c"
	ownershipId="StorageMediaEdge_StorageFiles"
/>

# How to check for old agent versions

1. Check if you already have an older version of the Agent installed on your server. 
2. If you do, uninstall the old agent from the server and try the agent installation.
3. You can get the current installed version from the following registry query in powerhshell.  
4. Open an Administrator powershell command prompt and run the following:

~~~powershell

Get-Itemproperty "HKLM:\SOFTWARE\Microsoft\Azure\StorageSync\Agent\" | Select Version

~~~

The output will give you the current version of Azure File Sync agent that is installed.

## **Recommended Documents**

1. [The current version of the Azure File Sync agent can be found here](https://www.microsoft.com/en-us/download/details.aspx?id=57159)
