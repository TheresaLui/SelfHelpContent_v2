<properties
    pageTitle="Unable to allocate a relative identifier error when trying to domain join account"
    description="Unable to allocate a relative identifier error when trying to domain join account"
    infoBubbleText="Unable to allocate a relative identifier error when trying to domain join account"
    service="Microsoft.Storage"
    resource="storageAccounts"
    authors="yagohel23"
    ms.author="yagohel"
    displayOrder=""
    selfHelpType="Diagnostics"
    supportTopicIds="32689882"
    resourceTags=""
    productPesIds="1003478"
    cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="1e2fc3b6-0a00-4309-b49f-cf02a8862e8f"
    ownershipID="Centennial_CloudNet_LoadBalancer"
/>

# Unable to allocate a relative identifier error when trying to domain join account

<!--issueDescription-->
User gets Unable to allocate a relative identifier error when trying to domain join account.
<!--/issueDescription-->

## **Recommended Steps**

When customer attempts to domain join an Azure Storage Account using the Join-AzStorageAccountforAuth powershell command the following error results:

**Error:**  "The directory service was unable to allocate a relative identifier" 

**Root Cause/Mitigation**

This problem may occur if a domain controller, that holds the operations master role of RID Master, is unavailable or was removed from the domain and restored from backup.  
**Next Steps:**  

1. Have the customer go to their Active Directory Users and Computers. Select the "domain controllers" container. 
2. Confirm with the customer that all DCs listed in the Domain Controllers container are running and available
3. If bringing the unavailable DC back on-line does not resolve the issue, collaborate with Directory Services  
4. More information for scenarios where a domain controller was restored from backup [explained here](https://support.microsoft.com/help/822053/error-message-windows-cannot-create-the-object-because-the-directory-s)
