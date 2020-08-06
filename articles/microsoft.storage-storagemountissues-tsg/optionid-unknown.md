<properties pageTitle="The option ID == is unknown"
            description="The option ID == is unknown"
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
            articleId="0b25e982-726c-460e-a80a-27c66e85e42a"
            ownershipId="Centennial_CloudNet_LoadBalancer" />

# The option ID == is unknown

**Symptom**

1. The customer is trying to map a network drive with net use. The Storage Account key contains a forward slash.
2. When they try to map the drive, they may receive an error message that resembles the following: The option ID == is unknown.

**Cause**

The Command Interpreter (cmd.exe) is interpreting everything after the forward slash (/) as a command line option

**Resolution**

To fix this issue, you can use PowerShell to map the network drive, as PowerShell will not interpret the forward slash as a command-line option


**Using PowerShell by itself**

```powershell
New-SmbMapping -LocalPath z: -RemotePath \\StorageAccountName.file.core.windows.net\sharename -UserName StorageAccountName -Password 'AccountPassword'
```

**Using PowerShell in a script**

You can invoke PowerShell from a script in the following way:

```powershell
Echo New-SmbMapping -LocalPath z: -RemotePath StorageAccountName.file.core.windows.net/sharename -UserName StorageAccountName -Password 'AccountPassword' | powershell -command -
```

*Note: The trailing '-' is required. Check forward slash and backslash*

<!---

---
**This is the end of the work flow. Did this TSG resolve your issue?**

1. Yes
2. No

-->