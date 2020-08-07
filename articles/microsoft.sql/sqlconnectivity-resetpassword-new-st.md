<properties
    pageTitle="How to questions: Reset password"
    description="How to questions: Reset password"
    service="microsoft.sql"
    resource="servers"
    authors="VMMicrosoft,subbu-kandhaswamy"
    ms.author="vimahadi,subbuk"
    displayOrder="1"
    selfHelpType="generic"
    supportTopicIds="32745437"
    productPesIds="13491"
    cloudEnvironments="public,blackForest,fairfax, usnat, ussec, mooncake"
    resourceTags="servers, databases"
    articleId="DAC21D19-C2C8-4E1F-8597-0ABC35261CB4"
    ownershipId="AzureData_AzureSQLDB_Availability"
/>

# How to questions: Reset password

## **Recommended Steps**

### How to questions: Reset password

The admin login name cannot be changed after it has been created. To reset the password for the server administrator
- Please go to your Azure portal
- Click SQL Servers
- Select the server from the list
- Click Reset Password.

You can also use PowerShell or the Azure CLI to reset the password.

For updating passwords from T-SQL, please follow instructions to [Alter Login](https://docs.microsoft.com/sql/t-sql/statements/alter-login-transact-sql?view=azuresqldb-current?WT.mc_id=pid:13491:sid:32745437/)

Visit [Strong Passwords](https://docs.microsoft.com/sql/relational-databases/security/strong-passwords?view=azuresqldb-current?WT.mc_id=pid:13491:sid:32745437/) for tips regarding setting strong passwords. <br>
