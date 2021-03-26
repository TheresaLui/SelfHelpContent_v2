<properties
pageTitle="How to Reset Admin or User Password/Credentials"
description="How to Reset Admin or User Password/Credentials"
ms.author="keithelm"
displayOrder=""
articleId="9c49b303-bdce-48c6-9cd7-005564280efb"
selfHelpType="Apollo"
supportTopicIds="3d780dd5-7558-b609-a634-c8221b70709d"
productPesIds="13491"
cloudEnvironments="public"
mappedToBucket="true"
ownershipId="AzureData_AzureSQLDB"
/>

# How to Reset Admin or User Password/Credentials
 

## How to Reset Admin or User Password/Credentials

The administrator password is reset by clicking *Reset Password* on the top menu bar of the Server blade. Depending on your screen width, you may need to click the ellipsis on the right side of the menu bar to see this option. Navigate to the server blade using the button below:

[Open server blade](button-data-context:SqlAzureExtension.ServerBlade.id.$resourceId)


The password for non-admin users can be changed using a client application such as SQL Server Management Studio or Azure Data Studio and the [ALTER LOGIN](https://docs.microsoft.com/sql/t-sql/statements/alter-login-transact-sql?view=azuresqldb-current?WT.mc_id=pid:13491:sid:32745437/) statement.

**Note:** The admin login name cannot be changed after it has been created.

## **Recommended Documents**

 - [Strong Passwords](https://docs.microsoft.com/sql/relational-databases/security/strong-passwords?view=azuresqldb-current?WT.mc_id=pid:13491:sid:32745437/)