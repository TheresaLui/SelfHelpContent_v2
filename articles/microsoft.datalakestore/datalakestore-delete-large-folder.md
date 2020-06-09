<properties
    pageTitle="ADLS Gen1 - Delete large folder"
    description="ADLS Gen1 - Delete large folder"
    service="Microsoft.DataLakeStore"
    resource="datalake"
    authors="sumantmehtams"
    ms.author="sumameh"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32674927"
    resourceTags=""
    productPesIds="15879"
    cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="18a84e7a-f7d1-4e36-ad2e-d4ee8fd4e5a9"
	ownershipId="StorageMediaEdge_DataLakeStorageGen1"
/>
 
# ADLS Gen1 - delete large folder
 

Recursive deletes of large subfolders in an ADLS Gen1 account may time out when the user performing the deletes is not a superuser. Recursive deletes require recursive enumeration of subfolders to perform ACL checks to ensure that the user has the required permissions to delete all files under the target folder.  
<br>

## **Recommended Steps**


1. Issue the recursive delete as a superuser. This will skip the recursive enumeration required for ACL checks.
2. If Step 1 is not possible, try to delete smaller sub-folders individually before deleting the parent folder

