<properties pageTitle="Disable Secure Transfer"
            description="Disable Secure Transfer"
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
            articleId="1067eecf-012e-4cca-bfeb-3dc13b2c9b45"
            ownershipId="Centennial_CloudNet_LoadBalancer" />

## **Recommended Steps**

### Disable Secure Transfer

**How to check Secure Transfer**

When you use the Azure Files service, any connection without encryption fails when Secure transfer required is enabled. This includes scenarios that use SMB 2.1, SMB 3.0 without encryption, and some versions of the Linux SMB client.

1. Sign in to Azure portal
2. Go to the storage account that hosts the Azure file share
3. Select Configuration, make sure that the Secure transfer required option is disabled

<!---

---
**Did disabling secure transfer solve the issue?**

1. Yes
2. No

-->
