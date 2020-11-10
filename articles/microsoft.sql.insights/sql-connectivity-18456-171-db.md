<properties
	pageTitle="Login failed due to invalid TLS version"
	description="Login failed due to invalid TLS version"
	infoBubbleText="The error returned indicated that login attempts failed from clients that are using a TLS version lower than the Minimal TLS Version of the server"
	service="microsoft.sql"
	resource="servers"
	ms.author="vitomaz"
	authors="vitomaz-msft"
	displayOrder=""
	articleId="sql_connectivity_18456_171_db"
	diagnosticScenario="SqlLtsFailedLogin"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLDB_Connectivity"
/>
# We ran diagnostics on your resource and found an issue

## **Login failed due to invalid TLS version**

<!--issueDescription-->
We ran diagnostics between <!--$StartTime-->StartTime<!--/$StartTime--> UTC and <!--$EndTime-->EndTime<!--/$EndTime--> UTC and we were able to detect login failures.
<br>

The error returned indicated that login attempts failed from clients that are using a TLS version lower than the Minimal TLS Version of the server.
<br>

<!--$FailedLogins18456State171DB--> FailedLogins18456State171DB <!--/$FailedLogins18456State171DB-->
<!--/issueDescription-->
<br>

The minimal Transport Layer Security (TLS) version setting allows customers to choose which version of TLS their SQL database uses.

Currently, we support TLS 1.0, 1.1, and 1.2. Setting a minimal TLS version ensures that newer TLS versions are supported. For example, choosing a TLS version greater than 1.1 means only connections with TLS 1.1 and 1.2 are accepted, and connections with TLS 1.0 are rejected. After you test to confirm that your applications support it, we recommend setting the minimal TLS version to 1.2. This version includes fixes for vulnerabilities in previous versions and is the highest version of TLS that's supported in Azure SQL Database.

After you set the minimal TLS version, login attempts from customers who are using a TLS version lower than the minimal TLS version of the server will fail.

## **Recommended Steps**

* For customers with applications that rely on older versions of TLS, we recommend setting the minimal TLS version according to the requirements of your applications. 

* For customers that rely on applications to connect by using an unencrypted connection, we recommend not setting any minimal TLS version.

* Please note that after you enforce a version of TLS, it's not possible to revert to the default.
 
## **Recommended Documents**

* [Minimal TLS version](https://docs.microsoft.com/azure/azure-sql/database/connectivity-settings#minimal-tls-version)