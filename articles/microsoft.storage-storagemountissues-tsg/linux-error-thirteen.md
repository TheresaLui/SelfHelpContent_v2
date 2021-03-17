<properties pageTitle="Mount error(13) 'Permission denied' when you try to mount the share from Linux"
            description="Mount error(13) 'Permission denied' when you try to mount the share from Linux"
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
            articleId="06263062-0c28-42f4-8b05-b638e9a1f836"
            ownershipId="Centennial_CloudNet_LoadBalancer" />

# Mount error(13) 'Permission denied' when you try to mount the share from Linux

**Cause**

Wrong username and/or password

**Resolution**

1. For Mount Error 13, verify the username and password
2. The username should be the name of the storage account, and the password has to be the correct Storage Account key

    Example:
    ```bash
    sudo mount -t cifs //StorageAccountName.file.core.windows.net/ShareName /mnt_bkp -o vers=3.0,user=StorageAccountName,password=StorageAccountKey dir_mode=0777,file_mode=0777,serverino
    ```

<!---

---

**This is the end of the work flow. Did this TSG resolve your issue?**

1. Yes
2. No

-->