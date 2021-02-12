<properties pageTitle="Cannot access 'FilePath'"
            description="Cannot access 'FilePath'"
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
            articleId="0e71ee85-406e-4e1d-a6c5-6d4f4eba64f7"
            ownershipId="Centennial_CloudNet_LoadBalancer" />

# Cannot access 'FilePath'

**Symptoms**

When you try to list files in an Azure file share by using ls command, ls command hangs when listing directory or you receive the following error:

```bash
'*ls: cannot access **'*****File*Path*** : **Input/output error**
```


**Cause**

Missing Linux OS fixes

**Resolution**

Upgrade the Linux kernel to the following versions that have fix for this issue:

1. 4.4.87+
2. 4.9.48+
3. 4.12.11+
4. All versions that is greater or equal to 4.13

<!---

---
**This is the end of the work flow. Did this TSG resolve your issue?**

1. Yes
2. No

-->