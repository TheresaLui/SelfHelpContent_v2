<properties
	pageTitle="Migrating to Azure|SQL Server migration assistant (SSMA)"
	description="Migrating to Azure|SQL Server migration assistant (SSMA)"
	service="microsoft.sql"
	resource="servers"
	authors="MladjoA"
    ms.author="mlandzic"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32637309"
	productPesIds="16259"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
    articleId="456e1f7b-0d4f-4f19-93ee-dc0885fb0f6e"
	ownershipId="AzureData_AzureSQLMI"
/>

# SQL Server migration assistant

Microsoft SQL Server Migration Assistant (SSMA) is a tool designed to automate database migration to SQL Server from Microsoft Access, DB2, MySQL, Oracle, and SAP ASE. It supports all versions of SQL Server as a target, up to the newest SQL Server 2019. There is no specific target version for Azure SQL Database Managed Instance, nor SSMA has built-in logic specific to Managed Instance.
SSMA can be used as a first step in migration to Managed Instance. Once database is migrated to SQL Server, additional assessment using [Database Migration Assistant](https://docs.microsoft.com/sql/dma/dma-overview) is recommended, before final migration using native backup/restore process or [Azure Database Migration Service](https://docs.microsoft.com/azure/dms/dms-overview).

## **Recommended Documents**

- [SQL Server Migration Assistant](https://docs.microsoft.com/sql/ssma/sql-server-migration-assistant)
- [Database Migration Assistant](https://docs.microsoft.com/sql/dma/dma-overview)
- [Azure Database Migration Service](https://docs.microsoft.com/azure/dms/dms-overview)
