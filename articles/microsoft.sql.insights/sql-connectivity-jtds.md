<properties
	pageTitle="Connections using unsupported driver (jTDS) detected"
	description="Connections using unsupported driver (jTDS) detected"
	infoBubbleText="Connections using unsupported driver (jTDS) detected"
	service="microsoft.sql"
	resource="servers"
	ms.author="vitomaz"
	authors="vitomaz-msft"
	displayOrder=""
	articleId="sql_connectivity_jtds"
	diagnosticScenario=""
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="13491"
	cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLDB_Connectivity"
/>
# We ran diagnostics on your resource and found an issue

## **Connections using unsupported jTDS driver**

<!--issueDescription-->
We ran diagnostics between <!--$StartTime-->StartTime<!--/$StartTime--> UTC and <!--$EndTime-->EndTime<!--/$EndTime--> UTC and we were able to detect connection attempts to database <!--$DatabaseName-->DatabaseName<!--/$DatabaseName--> on server <!--$ServerName-->ServerName<!--/$ServerName--> using jTDS, an unsupported driver.
<br>
<!--$jTDSInsightListOfApplications--> jTDSInsightListOfApplications <!--/$jTDSInsightListOfApplications-->
<!--/issueDescription-->

## **Recommended Steps**

To ensure stable, reliable, and secure connectivity, we strongly recommend that you update (or contact the application provider) to the latest version of a supported driver like [Microsoft JDBC Driver for SQL Server](https://docs.microsoft.com/sql/connect/jdbc/microsoft-jdbc-driver-for-sql-server). This driver is available at no additional charge and provides Java database connectivity from any Java application, application server, or Java-enabled applet. This driver is a Type 4 JDBC driver that provides database connectivity through the standard JDBC application program interfaces (APIs).  

Based on jTDS official documentation (http://jtds.sourceforge.net/), jTDS is an open-source 100% pure Java (type 4) JDBC 3.0 driver for Microsoft SQL Server (6.5, 7, 2000, 2005, 2008 and 2012). The last update on this driver was done in 2013 and it does not seem to be actively developed.  

Connection attempts using jTDS are not covered by our technical support.

## **Recommended Documents**

- [Microsoft JDBC Driver for SQL Server](https://docs.microsoft.com/sql/connect/jdbc/microsoft-jdbc-driver-for-sql-server)
- [Use Java and JDBC with Azure SQL Database](https://docs.microsoft.com/azure/azure-sql/database/connect-query-java)
