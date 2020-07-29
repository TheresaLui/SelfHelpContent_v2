<properties pageTitle="Check Azure regions for Storage Account and VM"
            description="Check Azure regions for Storage Account and VM"
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
            articleId="bdd729e9-09e4-4d7d-9c22-9d6f05e89987"
            ownershipId="Centennial_CloudNet_LoadBalancer" />

# Check Azure regions for Storage Account and VM

**How to check Azure regions for Storage Account and VM**

To check regions, go to Azure portal and select the Storage Account and/or VM then look at location field

PowerShell to check VMs name and region list:
```Powershell
Get-AzVm
```

PowerShell to check Storage accounts names and regions:</br>
```Powershell
Get-AzStorageAccount
```

<!---

---
**Where is the VM located?**

1. Local VM or different Azure region
2. Azure VM and Azure storage are same region

-->