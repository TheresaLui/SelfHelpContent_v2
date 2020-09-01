<properties
pageTitle="Troubleshoot Azure Files mount error 53 on Windows"
description="How to troubleshoot Azure Files Windows mount error 53"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="Storagev2insights_files_mount_windows_error53"
diagnosticScenario="Troubleshoot Azure Files mounting errors on Windows"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Azure Files - Windows mount error 53

<!--issueDescription-->
If your Azure file share mount fails with the following error: "System error 53 has occurred. The network path was not found", please follow the recommended steps below to troubleshoot the problem.
<!--/issueDescription-->

## **Recommended Steps**

**Cause: Port 445 is blocked**

System error 53 can occur if port 445 outbound communication to an Azure Files datacenter is blocked. To see the summary of ISPs that allow or disallow access from port 445, go to [TechNet](https://social.technet.microsoft.com/wiki/contents/articles/32346.azure-summary-of-isps-that-allow-disallow-access-from-port-445.aspx).

To check if your firewall or ISP is blocking port 445, use the [AzFileDiagnostics](https://gallery.technet.microsoft.com/Troubleshooting-tool-for-a9fa1fe5) tool or [Test-NetConnection](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-windows-file-connection-problems#cause-1-port-445-is-blocked) cmdlet. 

**Solutions**

- [Solution 1 - Use Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-windows-file-connection-problems#solution-1---use-azure-file-sync)
- [Solution 2 - Use VPN](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-windows-file-connection-problems#solution-2---use-vpn)
- [Solution 3 - Unblock port 445 with help of your ISP/IT Admin](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-windows-file-connection-problems#solution-3---unblock-port-445-with-help-of-your-ispit-admin)
- [Solution 4 - Use REST API based tools like Storage Explorer/Powershell](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-windows-file-connection-problems#solution-4---use-rest-api-based-tools-like-storage-explorerpowershell)

## **Recommended Documents**

- [Troubleshoot Azure Files problems in Windows](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-windows-file-connection-problems)
- [AzFileDiagnostics - Troubleshooting tool for Azure Files mounting errors on Windows](https://gallery.technet.microsoft.com/Troubleshooting-tool-for-a9fa1fe5)
- [Test-NetConnection cmdlet](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-windows-file-connection-problems#cause-1-port-445-is-blocked)
- [How to setup Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-extend-servers)
- [Instructions to setup VPN](https://github.com/Azure-Samples/azure-files-samples/tree/master/point-to-site-vpn-azure-files)
- [Storage Explorer](https://docs.microsoft.com/azure/vs-azure-tools-storage-manage-with-storage-explorer?tabs=windows)
- [PowerShell](https://docs.microsoft.com/azure/storage/files/storage-how-to-use-files-powershell)
