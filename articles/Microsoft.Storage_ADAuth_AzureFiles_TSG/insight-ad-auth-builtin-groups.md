<properties
    pageTitle="Customer is requesting information on storageaccount\user and storageaccount\Administrators groups"
    description="Customer is requesting information on storageaccount\user and storageaccount\Administrators groups"
    infoBubbleText="Customer is requesting information on storageaccount\user and storageaccount\Administrators groups"
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
    articleId="d0c0c253-5127-4b88-ae65-59c3cc01b16b"
    ownershipID="Centennial_CloudNet_LoadBalancer"
/>

# Customer is requesting information on storageaccount\user and storageaccount\Administrators groups

<!--issueDescription-->
After using robocopy to move their data to Azure File Share, customer will notice that  previously present BUILTIN\Administrators and BUILTIN\Users security descriptor now have StorageAccountName\Administrators and StorageAccountName\Users present in the security descriptor on the Azure File Share. They are requesting more details on this.
<!--/issueDescription-->
## **Recommended Action**

Customers are seeing that after robocopy, files that previously had the "BUILTIN\Administrators" and "BUILTIN\Users" present in the security descriptor now have "StorageAccountName\Administrators" and "StorageAccountName\Users" present in the security descriptor on the Azure File Share.  They are wondering what these groups mean in the context of AD users accessing an Azure Files file with a security descriptor that has permissions set for these BUILTIN groups.  

The answer is that these BUILTIN groups are not used in Azure Files, so no user is a member of them and no user can access files that have ACLs only for these built in groups.

To grant access to users to files that only have ACLs for these built in groups, customers should mount the file share using storage account name and key.  By mounting using storage account name and key, they mount as a super-user and bypass file-level access checks.  They then can set the ACLs to grant access to specific users or non "BUILTIN" groups.  For example, if customers want all users to be able to access the file, they can do the following icacls command:
     icacls <filepath>  /grant "Authenticated Users":F
