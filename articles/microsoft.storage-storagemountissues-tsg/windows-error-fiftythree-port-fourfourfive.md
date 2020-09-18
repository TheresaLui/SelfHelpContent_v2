<properties pageTitle="Check if port 445 is open"
            description="Check if port 445 is open"
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
            articleId="35537ed3-82b9-4005-ab7c-ce17926fca6b"
            ownershipId="Centennial_CloudNet_LoadBalancer" />

# Check if port 445 is open

**How to check if port 445 is open**


1. System error 53 or system error 67 can occur if port 445 outbound communication to an Azure Files datacenter is blocked
2. To check if your firewall or ISP is blocking port 445, use the Test-NetConnection cmdlet

    Sample script:

    ```powershell
    $resourceGroupName = $your-resource-group-name$
    $storageAccountName = $your-storage-account-name$

    # This command requires you to be logged into your Azure account, run Login-AzAccount if you haven't already logged in.
    $storageAccount = Get-AzStorageAccount -ResourceGroupName $resourceGroupName -Name $storageAccountName 

    # The ComputerName or host is $storage-account$.file.core.windows.net for Azure Public Regions. 
    # $storageAccount.Context.FileEndpoint is used because non-Public Azure regions, such as sovereign clouds or Azure Stack deployments, will have different hosts for Azure file shares and other storage resources. 

    Test-NetConnection -ComputerName ([System.Uri]::new($storageAccount.Context.FileEndPoint).Host) -Port 445
    ```

    If the connection was successful, you should see the following output: **TcpTestSucceeded:True**

<!---

---
**Is port 445 blocked or unblocked?**

1. Unblocked
2. Blocked

-->