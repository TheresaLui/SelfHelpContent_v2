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
    
For share-level authorization, Administrators assign permissions through the RBAC model in Portal.  A user may be authorized one or many of the following share-level permissions:
    
            FileShareFile_Read,
            FileShareFile_Write,
            FileShareFile_Delete,
            FileShareFile_ModifyPermission,
    
A user must have a SID present in their Kerberos ticket that corresponds to an OID present in the role definition for their subscription.  
    
For file-level authorization, the system uses NTFS ACLs on a per-file/directory basis.  A user must have a SID present in their Kerberos ticket that matches a SID authorized in the in the security descriptor for the file/directory object.  
    
To open a file for a certain permission (for example "write"), the user must have share-level write permissions as well as file-level write permissions.  

**Data to collect**

1. Ask the customer for their output for the security descriptor of the file.
        
        icalcls "fileOrdirectoryName"
        
2. Ask the customer for the output of "whoami /user" and "whoami /groups"

3. Identify OID corresponding to customer's AD Account and Ggab the storage account's role definition.This is available via Azure Support Center -> AD Explorer.

![](Screenshots\ASCAccountRoles.png)

4. Ask the customer to do graph lookup to get corresponding SIDs for their OIDs.

    a. Login to http://graphexplorer.azurewebsites.net/# as any azure user

    b. In the query space, enter as below. Modify the highlighted to match the OID for which you are trying to get corresponding on-prem SID.

      https://graph.windows.net/myorganization/users/41afbc1d-e326-41aa-b737-c7b46c2bbc3e

   ![GraphAPI.png](Screenshots\GraphAPI.png)

**Resolution**

1. Determine if the user has Share level access by verifying their RBAC permissions through ASC and verify their SID which we retrieved from Step 4 is part of the "whoami /user" or "whoami /groups" result. Provide appropriate RBAC permissions as required. 

2. Determine if the user has appropriate file/directory level NTFS permissions. Use the result of step 2 and verify one of the username is part of the result of step 1.