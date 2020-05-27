<properties
	pageTitle="security, privacy and compliance/missingauditing"
	description="security, privacy and compliance/missingauditing"
	infoBubbleText="Informational message about missing auditing data.  See details on the right."
	service="microsoft.sql"
	resource="servers"
	authors="fitzgeraldsw"
	ms.author="scfitzge"
	displayOrder="2"
	articleId="IsMissingAuditing_C355ADE8-6C0E-4F8E-8C2C-940F2196F1DA"
	diagnosticScenario="missingAuditData"
	selfHelpType="diagnostics"
	supportTopicIds="32630407"
	resourceTags="missingAuditing"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	ownershipId="AzureData_AzureSQLDB_Security"
/>

# Missing Auditing Data

<!--issueDescription-->
SQL database auditing  tracks database events and writes them to an audit log in your Azure storage account, Operations Management Suite (OMS) workspace, or Event Hubs. The audit session is removed when the database is removed from the replica and the audit session is started on the startup of the new replica.
<!--/issueDescription-->

This message is informational to make you aware of the gap in storage of auditing data.

## **Recommended Steps**

This message is informational to make you aware of the gap in storage of auditing data.

## **Recommended Documents**

* [Get started with SQL database auditing](https://docs.microsoft.com/azure/sql-database/sql-database-auditing)
