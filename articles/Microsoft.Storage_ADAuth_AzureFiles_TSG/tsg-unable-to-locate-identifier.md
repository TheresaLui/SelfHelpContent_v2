<properties
    pageTitle="Unable to allocate a relative identifier when trying to domain join account"
    description="Unable to allocate a relative identifier when trying to domain join account"
    service="Microsoft.Storage"
    resource="storageAccounts"
    authors="yagohel23"
    ms.author="yagohel"
    displayOrder=""
    selfHelpType="TSG_Content"
    supportTopicIds="32689882"
    resourceTags=""
    productPesIds="1003478"
    cloudEnvironments="public"
    articleId="1e2fc3b6-0a00-4309-b49f-cf02a8862e8f"
    ownershipID="Centennial_CloudNet_LoadBalancer"
/>

# User gets "Unable to allocate a relative identifier" error while trying to join Storage account to Active Directory Domain

## Symptoms

When customer attempts to domain join an Azure Storage Account using the Join-AzStorageAccountforAuth powershell command the following error results:

![](Screenshots\RElativeIdentifier1.png)

**Error:**  "The directory service was unable to allocate a relative identifier" 

**Root Cause/Mitigation**

This problem may occur if a domain controller, that holds the operations master role of RID Master, is unavailable or was removed from the domain and restored from backup.  

**Next Steps:**  

1. Have the customer go to their Active Directory Users and Computers.  Select the "domain controllers" container: 
![](Screenshots\RElativeIdentifier2.png)
2. Confirm with the customer that all DCs listed in the Domain Controllers container are running and available.   
3. If bringing the unavailable DC back on-line does not resolve the issue, collaborate with Directory Services  
4. More information for scenarios where a domain controller was restored from backup:

   i.  https://support.microsoft.com/help/822053/error-message-windows-cannot-create-the-object-because-the-directory-s 