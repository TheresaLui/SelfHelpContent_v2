<properties pageTitle="Quota Exceeded (Error 1816)"
            description="Quota Exceeded (Error 1816)"
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
            articleId="a48d3b12-0f7e-48a2-9a22-1cd4f515afb2"
            ownershipId="Centennial_CloudNet_LoadBalancer" />

# Quota Exceeded (Error 1816)

Error Not enough quota is available to process this command when trying to open an Azure Files share. Possible errors include:

1. 1816 ERROR_NOT_ENOUGH_QUOTA
2. 0xc0000044 STATUS_QUOTA_EXCEEDED
3. Invalid handle value GetLastError: 53
4. Linux error: [permission denied]
5. Linux error: Disk quota exceeded

If you see the following in a network trace, it indicates the customer has reached the upper limit on the number of SMB-based requests:

1. XS_STATUS_SMB_TOO_MANY_HANDLES or
2. XS_STATUS_SMB_TOO_MANY_LOCKS or
3. XS_STATUS_SMB_TOO_MANY_NOTIFICATIONS

Most times the issue seems to occur when the number of concurrent open handles for a file or a folder reaches the upper limit at Azure File storage.

The maximum handles per file or folder is 2000 (as of 12/6/2016) at the Azure File storage level, when exceeded the STATUS_QUOTA_EXCEEDED followed by closing the mount point or share.

Customer might have an application which could be opening and closing a file or a folder, and in the process may not be closing the file or the folder properly (a handle leak), thus getting into this issue.

Customer needs to identify the Process/Daemon/Application/Code which creates such requests and reduce the number of concurrent open handles by closing some handles and retry. The next approaches can help you investigate further the issue.

**Using Azure Support Center**

1. Go to ASC > resource explorer > find storage account > file tab > search file handle
2. Input the Azure File Share, Directory or File to search for the handle amount. Format: {fileshare}/{file or directory path}
3. Review the report for all open handles
4. Search Directory Handles for an AFS in ASC
5. Instruct the customer to ensure that all unnecessary handles are closed
6. With customer consent, you may proceed to Force closure of a handle or Force the closure of all handles
7. Create ICM with the details of the Handle/s to be closed and Storage Account information [ICM Template](https://icm.ad.msft.net/imp/v3/incidents/create?tmpl=RK24oB)

	**Use windows tools**

	You can use [Handle.exe](https://docs.microsoft.com/sysinternals/downloads/handle) on a Windows client to check if there are open handles on the client against the Azure File share. Example below:

	```powershell
    handle $StorageAccountName$.file.core.windows.net
    ```


	If you are member of project TM-CSSStgRec Auto assign the ICM. Proceed to open the 'Force close handle' link in the ASC report or execute the Jarvis Action XStore-> Resource Property Retrieval -> [Force Close File Handle Operation](https://jarvis-west.dc.ad.msft.net/58B0211D?genevatraceguid=ecec0968-55a6-4621-bb0e-9d5c2baaf3e3)

8. Force Closure of a Single handle using Jarvis Actions

	Use the 'Get Access' button to generate the JIT request

9. Complete the JIT request by filling the 'Work-item Id' field with the previously created ICM, select the Access Level as PlatformServiceOperator and submit it. The other fields should auto-populate.

	Execute the query
    
    *Note: Jarvis Actions should automatically refresh after successfully creating the JIT request. Confirm with Customer that the handle is released and the file/s can be deleted. Resolve the ICM if issue is resolved.*

<!---

---
**This is the end of the work flow. Did this TSG resolve your issue?**

1. Yes
2. No

-->