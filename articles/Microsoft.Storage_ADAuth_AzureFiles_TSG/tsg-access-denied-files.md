<properties
    pageTitle="Access denied while trying to access files"
    description="Access denied while trying to access files"
    infoBubbleText="Access denied while trying to access files"
    service="microsoft.storage"
    resource="storageAccounts"
    authors="yagohel23"
    ms.author="yagohel"
    displayOrder=""
    selfHelpType="Diagnostics"
    supportTopicIds="32689882"
    resourceTags=""
    productPesIds="1003478"
    cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="121e0513-363c-4f7b-8e68-b9c6078e4137"
    ownershipID="Centennial_CloudNet_LoadBalancer"
/>

# Access denied while trying to access files/directory

<!--issueDescription-->
Access denied while trying to access files/directory
<!--/issueDescription-->

## **Recommended Steps**

Accessing a file or directory when using Azure Files with identity-based authentication requires two levels of authorization 1) share-level and 2) file/directory object-level.
    
For share-level authorization, Administrators assign permissions through the RBAC model in Portal. For more details, see here: https://docs.microsoft.com/azure/storage/files/storage-files-identity-ad-ds-assign-permissions
    
For file-level authorization, the system uses NTFS ACLs on a per-file/directory basis.  A user must have a SID present in their Kerberos ticket that matches a SID authorized in the in the security descriptor for the file/directory object. For more details, see here: https://docs.microsoft.com/azure/storage/files/storage-files-identity-ad-ds-configure-permissions 
    
To open a file for a certain permission (for example "write"), the user must have share-level write permissions as well as file-level write permissions.  

**Things to check**

1. Ask the customer for their output for the security descriptor of the file.
        
        icacls "fileOrdirectoryName"
        
2. Ask the customer for the output of "whoami /user" and "whoami /groups"

3. Verify the RBAC permissions customer has on their storage account. This can be done through ASC Resource Explorer as shown below. See here: https://supportability.visualstudio.com/AzureVMPOD/_wiki/wikis/AzureVMPOD/295083/ADAuth-for-Azure-Files-Access-Denied.md?anchor=things-to-check

**Resolution**

Based on the RBAC and NTFS permissions customer has in place, they will have the following permissions on a file/directory.

|                      | RBAC - None   | RBAC - SMB Reader | RBAC Contributor                 | RBAC SMB Elevated                                                                  |
|----------------------|---------------|-------------------|----------------------------------|------------------------------------------------------------------------------------|
| NTFS -None           | Access Denied | Access Denied     | Access Denied                    | Access Denied                                                                      |
| NTFS - Read          | Access Denied |        Read       |               Read               |                                        Read                                        |
| NTFS - Run & Execute | Access Denied |        Read       |               Read               |                                        Read                                        |
| NTFS - List Folder   | Access Denied |        Read       |               Read               |                                        Read                                        |
| NTFS - Write         | Access Denied |        Read       |        Read,   Run, Write        |           Read,   Write,       Apply Permissions to your own folder/files          |
| NTFS - Modify        | Access Denied |        Read       | Read,   Write,       Run, Delete | Read,   Write,       Run, Delete,       Apply Permissions to your own folder/files |
| NTFS - Full          | Access Denied |        Read       | Read,   Write,       Run, Delete |    Read,   Write, Run,       Delete, Apply Permissions to anyone's folders/files   |

1. Determine if the user should have share access by verifying the RBAC permissions.

2. Determine if the user should have file/directory access by verifying the NTFS permissions.  

If the user does not have appropriate permissions, please work with them to provide user necessary RBAC/NTFS permissions by referring to the table above. 
