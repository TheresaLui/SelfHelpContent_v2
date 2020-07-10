<properties
    pageTitle="Customer faces access denied issues while trying to use robocopy to move files."
    description="Customer faces access denied issues while trying to use robocopy to move files."
    infoBubbleText="Customer faces access denied issues while trying to use robocopy to move files."
    service="microsoft.storage"
    resource="storageAccounts"
    authors="yagohel23"
    ms.author="yagohel"
    displayOrder=""
    selfHelpType="Diagnostics"
    supportTopicIds="32689882"
    resourceTags=""
    productPesIds="1003478"
    cloudEnvironments="public,fairfax,blackforest,mooncake,usnat,ussec"
    articleId="599ed2f0-d2ae-4666-ae68-a632dd15a0c9"
    ownershipID="Centennial_CloudNet_LoadBalancer"
/>

# Customer faces access denied issues while trying to use robocopy to move files

<!--issueDescription-->
Customer faces access denied issues while trying to use robocopy to move files.
<!--/issueDescription-->

## **Recommended Steps**

It is a common scenario to robocopy files between file servers.  Unfortunately, this scenario is broken using AD Authentication for Azure Files in preview.

Whenever a request to add a file comes in to Azure Files, if the request is over a Kerberos (authenticated via AD) session, an access check happens to see if the caller has permissions to add a file under the parent directory of the file.  

For example, if a user is using robocopy with "/sec", when robocopy transfers a file to the destination, the following access checks occur.

1. Does the AD user executing robocopy have the permission to add a file or directory under the file's parent?
    a. This checks if FILE_ADD_FILE permission is granted to the user in the file's parent directory.
2. Does the AD user executing robocopy have the permission to set an ACL on the file?
    a. This checks if the user has WRITE_DAC permission to the file.
3. Does the AD user executing robocopy have the permission to set the owner on the file?
    a. This checks if the user has WRITE_OWNER permission to the file.

Unfortunately, with check #3, there is currently no AD user that has "Take Ownership" permission on the file share and can set the owner.  So if robocopy requires setting the owner, it will fail with access denied.  

We understand that this is a limitation in our functionality for the preview release and are addressing this before the feature becomes generally available.  We are working on a feature that will add a "Take Ownership" RBAC permission for AD users to be authorized for.

The recommended solution for those affected by this missing functionality is to execute any robocopy after mounting the file share using storage account and key.  When a user mounts via storage account and key, they mount as "super-users" and all access checks are skipped.

**Further Troubleshooting -  Log Collection**

If the customer would like to take trace and better understand if they are failing check #3 (or if for some reason mounting as storage account and key and copying the files fails as well), they can take the following trace.

1. Download Process Monitor from https://docs.microsoft.com/sysinternals/downloads/procmon
2. Open process monitor and add a filter for robocopy process.
3. Run robocopy targeted to Azure file share  with the additional parameter "/log:(LogFile)"

    a. More information about the robocopy logfile is [here](https://docs.microsoft.com/windows-server/administration/windows-commands/robocopy)
4. After robocopy gives error (or somehow works) save the process monitor log to a file.

    a. Specify "Events displayed using current filter"
5. Analyze the robocopy log file (specified as /log in the robocopy command) along with the process monitor logs.

    a. You may see that a IRP_MJ_CREATE request fails with access denied.  Check if desired access contains "write owner" type of access request.

        i. 11:57:13.4620871 AM    robocopy.exe    162116    IRP_MJ_CREATE    F:\CxCache\Corext.Tools.3.0.1\X86\robocopy.exe    SUCCESS    Desired Access: Generic Read, Write Owner Disposition: Open, Options: Synchronous IO Non-Alert, Non-Directory File, Attributes: n/a, ShareMode: Read, Write, Delete, AllocationSize: n/a, OpenResult: Opened    11444
             
        ii. If WRITE_OWNER type access fails, it's due to check #3 not being supported for AD users.