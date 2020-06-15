<properties pageTitle="Options around port 445"
            description="Options around port 445"
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
            articleId="e4cb04da-659e-4749-a815-0fd49e577ef3"
            ownershipId="Centennial_CloudNet_LoadBalancer" />

# Options around port 445

1. Use Azure File Sync
Azure File Sync can transforms your on-premises Windows Server into a quick cache of your Azure file share. You can use any protocol that's available on Windows Server to access your data locally, including SMB, NFS, and FTPS. Azure File Sync works over port 443 and can thus be used as a workaround to access Azure Files from clients that have port 445 blocked. <a href="https://docs.microsoft.com/en-us/azure/storage/files/storage-sync-files-extend-servers">Learn how to setup Azure File Sync</a>

2. Use VPN
<br>By Setting up a VPN to your specific Storage Account, the traffic will go through a secure tunnel as opposed to over the internet. Follow the <a href="https://github.com/Azure-Samples/azure-files-samples/tree/master/point-to-site-vpn-azure-files">instructions to setup VPN</a> to access Azure Files from Windows.</br>
<br>Work with your IT department or ISP to open port 445 outbound to <a href="https://www.microsoft.com/en-us/download/details.aspx?id=41653">Azure IP ranges</a></br>

3. Use REST API based tools like Storage Explorer/PowerShell
Azure Files also supports REST in addition to SMB. REST access works over port 443 (standard tcp). There are various tools that are written using REST API which enable rich UI experience. Storage Explorer is one of them. <a href="https://azure.microsoft.com/en-us/features/storage-explorer/">Download and Install Storage Explorer</a> and connect to your file share backed by Azure Files. You can also use PowerShell which also user REST API.

<!---

---
**This is the end of the work flow. Did this TSG resolve your issue?**

1. Yes
2. No

-->