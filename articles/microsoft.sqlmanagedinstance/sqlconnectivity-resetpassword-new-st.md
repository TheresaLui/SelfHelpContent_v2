<properties
    pageTitle="How to questions: Reset password"
    description="How to questions: Reset password"
    service="microsoft.sql"
    resource="managedinstances"
	authors="vitomaz-msft"
	ms.author="vitomaz"
    displayOrder="1"
    selfHelpType="generic"
    supportTopicIds="32746117"
    productPesIds="16259"
    cloudEnvironments="public,blackForest,fairfax,usnat,ussec,mooncake"
    resourceTags=""
    articleId="sqlmi-sqlconnectivity-resetpassword-new-st"
    ownershipId="AzureData_AzureSQLMI"
/>

# How to questions: Reset password

The password for the Server admin can be reset using the Azure portal.<br>
- Go to your Azure portal
- Click SQL Servers
- Select the server from the list
- Click Reset Password.

The password for non-admin users can be changed using a client application such as SQL Server Management Studio or Azure Data Studio and the [ALTER LOGIN](https://docs.microsoft.com/sql/t-sql/statements/alter-login-transact-sql?view=azuresqldb-current?WT.mc_id=pid:13491:sid:32745437/) statement.

**Note:** The admin login name cannot be changed after it has been created.

## **Recommended Documents**

 - [Strong Passwords](https://docs.microsoft.com/sql/relational-databases/security/strong-passwords?view=azuresqldb-current?WT.mc_id=pid:13491:sid:32745437/)<br>
