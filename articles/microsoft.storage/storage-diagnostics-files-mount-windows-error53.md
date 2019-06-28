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
cloudEnvironments="public"
/>

# Azure Files - Windows mount error 53

<!--issueDescription-->
If your Azure file share mount fails with the following error: **_System error 53 has occurred. The network path was not found_**, please follow the recommended steps below to troubleshoot the problem.

## **Recommended Steps**

### **Cause: Port 445 is blocked**
System error 53 can occur if port 445 outbound communication to an Azure Files datacenter is blocked. To see the summary of ISPs that allow or disallow access from port 445, go to [TechNet](https://social.technet.microsoft.com/wiki/contents/articles/32346.azure-summary-of-isps-that-allow-disallow-access-from-port-445.aspx).

To check if your firewall or ISP is blocking port 445, use the [AzFileDiagnostics](https://gallery.technet.microsoft.com/Troubleshooting-tool-for-a9fa1fe5) tool or [Test-NetConnection](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-windows-file-connection-problems#cause-1-port-445-is-blocked) cmdlet. 

### **Solution**

#### Solution 1 - Use Azure File Sync
Azure File Sync can transforms your on-premises Windows Server into a quick cache of your Azure file share. You can use any protocol that's available on Windows Server to access your data locally, including SMB, NFS, and FTPS. Azure File Sync works over port 443 and can thus be used as a workaround to access Azure Files from clients that have port 445 blocked. [Learn how to setup Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-extend-servers).

#### Solution 2 - Use VPN
By Setting up a VPN to your specific Storage Account, the traffic will go through a secure tunnel as opposed to over the internet. Follow the [instructions to setup VPN](https://github.com/Azure-Samples/azure-files-samples/tree/master/point-to-site-vpn-azure-files) to access Azure Files from Windows.

#### Solution 3 - Unblock port 445 with help of your ISP/IT Admin
Work with your IT department or ISP to open port 445 outbound to [Azure IP ranges](https://www.microsoft.com/download/details.aspx?id=41653).

#### Solution 4 - Use REST API based tools like Storage Explorer/Powershell
Azure Files also supports REST in addition to SMB. REST access works over port 443 (standard tcp). There are various tools that are written using REST API which enable rich UI experience. [Storage Explorer](https://docs.microsoft.com/azure/vs-azure-tools-storage-manage-with-storage-explorer?tabs=windows) is one of them. [Download and Install Storage Explorer](https://azure.microsoft.com/features/storage-explorer/) and connect to your file share backed by Azure Files. You can also use [PowerShell](https://docs.microsoft.com/azure/storage/files/storage-how-to-use-files-powershell) which also user REST API.

<!--/issueDescription-->

## **Recommended Documents**

- [Troubleshoot Azure Files problems in Windows](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-windows-file-connection-problems)
- [AzFileDiagnostics - Troubleshooting tool for Azure Files mounting errors on Windows](https://gallery.technet.microsoft.com/Troubleshooting-tool-for-a9fa1fe5)
- [Test-NetConnection cmdlet](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-windows-file-connection-problems#cause-1-port-445-is-blocked)
- [How to setup Azure File Sync](https://docs.microsoft.com/azure/storage/files/storage-sync-files-extend-servers)
- [Instructions to setup VPN](https://github.com/Azure-Samples/azure-files-samples/tree/master/point-to-site-vpn-azure-files)
- [Storage Explorer](https://docs.microsoft.com/azure/vs-azure-tools-storage-manage-with-storage-explorer?tabs=windows)
- [PowerShell](https://docs.microsoft.com/azure/storage/files/storage-how-to-use-files-powershell)
