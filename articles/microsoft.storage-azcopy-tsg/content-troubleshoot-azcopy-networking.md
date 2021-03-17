<properties
	pageTitle="Troubleshoot AzCopy Networking"
	description="Troubleshoot AzCopy Networking"
        service="Microsoft.Storage"
        resource="Microsoft.Storage/storageAccounts"
	authors="rimayber"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="50e40b09-0ad5-40c8-855a-320093fc0678"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Troubleshoot AzCopy Networking

1. To configure the proxy settings for AzCopy, set the **https_proxy** environment variable. 
2. If you run AzCopy on Windows, AzCopy automatically detects proxy settings, so you don't have to use this setting in Windows. 
3. If you choose to use this setting in Windows, it will override automatic detection.

| Operating System |  Command  |
| ----------- | ----------- |
| Windows    |  In a command prompt use: **set https_proxy=<proxy IP>:<proxy port>** In PowerShell use: **$env:https_proxy="<proxy IP>:<proxy port>"**  |
| Linux   | **export https_proxy=<proxy IP>:<proxy port>**    |
| PMacOS   | **export https_proxy=<proxy IP>:<proxy port>**      |

*Note: Currently, AzCopy doesn't support proxies that require authentication with NTLM or Kerberos.*

### Network error prevention (TCP errors)

We encourage the use of HTTPS for all AzCopy traffic. While the primary reason is security, HTTPS also has the side effect of providing another layer of "error detection" on top of TCP's built-in detection. HTTPS has this effect because it's a tamper-resistant protocol. By preventing anyone deliberately changing your data as it crosses the network, HTTPS also prevents network errors from accidentally changing your data.

Oftentimes, setting the AZCOPY_CONCURRENCY_VALUE to auto is good solution to address TCP errors. However, if your AzCopy job will last less than a few minutes AUTO, as currently implemented, is not a good choice.  
