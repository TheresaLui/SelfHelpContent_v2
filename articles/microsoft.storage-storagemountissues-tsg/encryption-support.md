<properties pageTitle="Encryption support"
            description="Encryption support"
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
            articleId="58c2f87e-6784-4d21-bdd0-727998448271"
            ownershipId="Centennial_CloudNet_LoadBalancer" />

# Encryption support

**Symptom**

You receive an error message 'You are copying a file to a destination that does not support encryption' on a window display when trying to copy a file

**Cause**

1. Bitlocker-encrypted files can be copied to Azure Files. However, the File storage does not support NTFS EFS
2. Therefore, you are likely using EFS in this case
3. If you have files that are encrypted through EFS, a copy operation to the File storage can fail unless the copy command is decrypting a copied file

**Resolution**

To copy a file to the File storage, you must first decrypt it. You can do this by using one of the following methods:

1.  Use copy /d
2.  Set the following registry key:
    1. Path=HKLM\Software\Policies\Microsoft\Windows\System
    2. Value type=DWORD
    3. Name = CopyFileAllowDecryptedRemoteDestination
    4. Value = 1


*Note: Setting the registry key affects all copy operations to network shares*

<!---

---
**This is the end of the work flow. Did this TSG resolve your issue?**

1. Yes
2. No

-->