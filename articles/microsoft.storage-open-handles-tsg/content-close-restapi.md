<properties
	pageTitle="Query/Close handles using REST API"
	description="Query/Close handles using REST API"
	service="microsoft.storage"
	resource="storageAccounts"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="557c9a14-6092-4e41-9b06-5e706879eb12"
/>

# Query/Close handles using REST API

Find below the information about how you can query and close opened handles for Azure File Shares using REST API

**Get the list of open file handles**

1. **Use [List Handles](https://docs.microsoft.com/en-us/rest/api/storageservices/list-handles)**

~~~powershell

Method: GET
Request URI: https://myaccount.file.core.windows.net/myshare/mydirectorypath/myfileordirectory?comp=listhandles

~~~

**Close open file handles**

1. **Use [Force Close Handles](https://docs.microsoft.com/en-us/rest/api/storageservices/force-close-handles)**


~~~powershell

Method: PUT
Request URI: https://myaccount.file.core.windows.net/myshare/mydirectorypath/myfileordirectory?comp=forceclosehandles

~~~
