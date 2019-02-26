<properties
	pageTitle="security, privacy and compliance/access control"
	description="security, privacy and compliance/access control"
	service="microsoft.sql"
	resource="servers"
	authors="emlisa"
    authorAlias="emlisa"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32630403"
	resourceTags=""
	productPesIds="13491"
	cloudEnvironments="public"
    articleId="106ae851-713c-45b6-9ab9-f36ecfc976e2"
/>

# Access Control


## **Recommended steps**

### Do the following steps to add or remove a user's access
1. Use the following [command](https://docs.microsoft.com/powershell/module/azuread/get-azureadusermembership?view=azureadps-2.0?WT.mc_id=pid:13491:sid:32630403/) to get the Azure AD user’s permissions. <br>
2. To understand the user's role look at the corresponding [description.](https://docs.microsoft.com/sql/relational-databases/security/authentication-access/database-level-roles?view=sql-server-2017?WT.mc_id=pid:13491:sid:32630403/). <br>
3. If you are not already an Azure Active Directory administrator for your Azure SQL Database server, [follow these steps](https://docs.microsoft.com/azure/sql-database/sql-database-aad-authentication-configure#provision-an-azure-active-directory-administrator-for-your-azure-sql-database-server?WT.mc_id=pid:13491:sid:32630403/). Adding an admin must happen on Azure Active Directory. Do this if you want to use Azure AD accounts to connect to SQL Database. <br>
4. Follow [these steps](https://docs.microsoft.com/azure/sql-database/sql-database-manage-logins#additional-server-level-administrative-roles?view=sql-server-2017?WT.mc_id=pid:13491:sid:32630403/) to use the server admin role. This outlines a T-SQL script to create a new user.


## **Recommended Documents**

### What access control can be done at the serer level?
 
* Roles cannot be made at the [server level](https://docs.microsoft.com/sql/relational-databases/security/authentication-access/create-a-server-role?view=sql-server-2017&viewFallbackFrom=sql-server-2017?WT.mc_id=pid:13491:sid:32630403/), they must be made at the database level. <br>
* The only way to change the server admin login is to recreate a new logical server. If there are already user databases created, you can [export](https://docs.microsoft.com/azure/sql-database/sql-database-export?view=sql-server-2017?WT.mc_id=pid:13491:sid:32630403/) the database as bacpac files and [import](https://docs.microsoft.com/azure/sql-database/sql-database-import?view=sql-server-2017?WT.mc_id=pid:13491:sid:32630403/) them from bacpac file in the new server.


### Other access control documents

* [Firewall and firewall rules](https://docs.microsoft.com/azure/sql-database/sql-database-control-access#firewall-and-firewall-rules?WT.mc_id=pid:13491:sid:32630403/)<br>
* [Authentication](https://docs.microsoft.com/azure/sql-database/sql-database-control-access#authentication?WT.mc_id=pid:13491:sid:32630403/)<br>
* [Authorization](https://docs.microsoft.com/azure/sql-database/sql-database-control-access#authorization?WT.mc_id=pid:13491:sid:32630403/)
