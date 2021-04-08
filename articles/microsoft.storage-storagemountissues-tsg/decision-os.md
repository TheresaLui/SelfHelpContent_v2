<properties pageTitle="Check the operating system having issues"
            description="Check the operating system having issues"
            service="Microsoft.Storage"
            resource="Microsoft.Storage/storageAccounts"
            authors="akshaymatmicrosoft"
            ms.author="akshaym"
            displayOrder=""
            selfHelpType="TSG_Content"
            supportTopicIds=""
            resourceTags=""
            productPesIds=""
            cloudEnvironments="public, fairfax, usnat, ussec"
            articleId="baff0ff8-728d-451b-84e7-752c029afeb1"
            ownershipId="Centennial_CloudNet_LoadBalancer" />

# Check the operating system having issues

**How to check the operating system having issues**

Consult with the customer to identify the source operating system that is having azure files mount issues. 

Verify if SMB or NFS? If latter, refer to [NSF v4 for Azure Files](https://supportability.visualstudio.com/AzureVMPOD/_wiki/wikis/AzureVMPOD/357136/NFS_v_4_for_Azure_Files).

For Azure AD DS files scenarios see [Azure Files AAD DS Integration](https://supportability.visualstudio.com/AzureVMPOD/_wiki/wikis/AzureVMPOD/265509/Azure-Files-AAD-DS-Integration). 

Alternatively, run 'edit & re-run' to surface **AD Auth for Azure Files Issues** TSG for on-premises scenario. 

<!--

---

**What is the OS you are troubleshooting in this case?**

1. Linux
2. Windows

-->