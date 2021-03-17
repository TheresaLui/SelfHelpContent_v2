<properties
	pageTitle="Storage Account Firewall - (403) Forbidden or (401) Unauthorized "
	description="Storage Account Firewall - (403) Forbidden or (401) Unauthorized "
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
	articleId="8284069b-5c1e-4363-a112-7afacf226531"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Storage Account Firewall - (403) Forbidden or (401) Unauthorized 

1. You receive the following error(s) when moving data to or across Storage Account(s) with AzCopy v10 that has Storage Account Firewall enabled.
2. Causes
    1. Azure Storage Firewall has been configured and customer's IP/subnet has not been granted access.
    2. Incorrect Storage Account Key and/or Storage Account name
    3. Invalid SAS token
3. Solution
    1. Verify Firewalls and Virtual networks settings on storage account. Consider source and destination account settings. 
    2. Make sure that the Storage Account name is correct, and has not been mistyped. The above error messages can also be seen if the Storage Account name is not correct.
    3. If you are using SAS, make sure that it?s not expired, for more information see [Using shared access signatures(SAS)](https://docs.microsoft.com/en-us/rest/api/storageservices/delegate-access-with-shared-access-signature).

## Recommended Documents

* [AzCopy v10 TSG](https://supportability.visualstudio.com/AzureVMPOD/_wiki/wikis/AzureVMPOD/265496/AzCopy-v10)
* [Internal Wiki](https://supportability.visualstudio.com/AzureVMPOD/_wiki/wikis/AzureVMPOD/302658/Azure_Storage_TSG_AzCopy-v10-TSG-Storage-Account-Firewall-(403)-Forbidden-or-(401)-Unauthorized)
