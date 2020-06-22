<properties pageTitle="Lost time stamps"
            description="Lost time stamps"
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
            articleId="b3b2b8e4-4c5b-4133-b2c0-f6d4b69dab14"
            ownershipId="Centennial_CloudNet_LoadBalancer" />


# Lost time stamps

**Symptoms**

Time stamps were lost in copying files from Windows to Linux. On Linux/Unix platforms, the cp -p command fails if file 1 and file 2 are owned by different users

**Cause**

The force flag f in COPYFILE results in executing cp -p -f on Unix. This command also fails to preserve the time stamp of the file that you don't own

**Workaround**

Use the storage account user for copying the files:

1. Useadd : [storage account name]
2. Passwd [storage account name]
3. su [storage account name]
4. cp -p filename.txt /share

<!---

---
**This is the end of the work flow. Did this TSG resolve your issue?**

1. Yes
2. No

-->