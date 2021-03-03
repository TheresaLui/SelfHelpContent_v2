<properties
	pageTitle="Customer userID belongs to multiple subscriptions/tenants"
	description="Customer userID belongs to multiple subscriptions/tenants"
        service="Microsoft.Storage"
        resource="Microsoft.Storage/storageAccounts"
	authors="rimayber"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="df766509-af03-499e-b92a-416f19a23cbf"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Customer userID belongs to multiple subscriptions/tenants

If you intend to authenticate with **AAD**, it's imperative you ensure you're logged into the correct tenant. 

At the command prompt: 

~~~shell

azcopy login 
azcopy login **--tenant-id=<tenant-id>**

~~~

*Note: Assign requisite [RBAC](https://docs.microsoft.com/en-us/azure/storage/common/storage-auth-aad-rbac-portal?toc=%2fazure%2fstorage%2fblobs%2ftoc.json) permissions*
