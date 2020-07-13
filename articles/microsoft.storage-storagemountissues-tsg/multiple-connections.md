<properties pageTitle="Multiple connections"
            description="Multiple connections"
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
            articleId="4784446c-225d-4145-8bff-1e6b455d2e20"
            ownershipId="Centennial_CloudNet_LoadBalancer" />

# Multiple connections

**Symptom**

Error: 'Multiple connections to a server or shared resource by the same user, using more that one user name, are not allowed' when access the mounted File share drive

**Resolution**

1. First, add the Storage Account user with cmdkey, but provide a domain name of 'AZURE.' For example:
    ```dos
    cmdkey /add:StorageAccount.file.core.windows.net /user:AZURE\StorageAccount /pass:[Password]
    ```

2. Then, when mapping the drive, use the /savecred option, and do not specify a username:
    ```dos
    net use K: \\StorageAccount.file.core.windows.net\sharename
    ```

<!---

---
**This is the end of the work flow. Did this TSG resolve your issue?**

1. Yes
2. No

-->