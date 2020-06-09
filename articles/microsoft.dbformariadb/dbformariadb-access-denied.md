<properties
	pageTitle="Orcas MariaDB Server Login Failed with Access Denied"
	description="RCA - Login Failed with Access Denied"
	infoBubbleText="Login Failed with Access Denied detected. See details on the right"
	service="microsoft.dbformariadb"
	resource="dbformariadb"
	authors="congwang"
	ms.author="conwan"
	displayOrder="100"
	articleId="dbformariadb-access-denied"
	diagnosticScenario="OrcasMariaDBAccessDenied"
	selfHelpType="rca"
	resourceTags="servers, databases"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforMariaDB"
/>
# Can't connect MariaDB database server because Access Denied

<!--issueDescription-->
During our investigation regarding connection issues to your MariaDB server <!--$ServerName-->ServerName<!--/$ServerName--> we found that <!--$Count-->Count<!--/$Count--> connection attempts to fail due to Access Denied error between <!--$StartTime-->StartTime<!--/$StartTime--> and <!--$EndTime-->EndTime<!--/$EndTime--> (UTC). An Access denied error can have many causes. Often the problem is related to the MariaDB accounts that the server permits client programs to use when connecting.
<!--/issueDescription-->

## **Recommended Steps**

An Access denied error can have many causes. Often the problem is related to the MariaDB accounts that the server permits client programs to use when connecting. See the following document for better understanding.

## **Recommended Documents**

* [Access Control and Account Management](https://dev.mysql.com/doc/refman/5.6/en/access-control.html)
* [Troubleshooting Problems Connecting to MySQL ](https://dev.mysql.com/doc/refman/5.6/en/problems-connecting.html)
