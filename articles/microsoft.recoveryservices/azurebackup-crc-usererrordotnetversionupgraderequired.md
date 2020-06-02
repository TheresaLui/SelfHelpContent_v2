<properties
    pageTitle="usererrordotnetversionupgraderequired"
    description="usererrordotnetversionupgraderequired"
    infoBubbleText="Azure Backup for SQL Server requires .NET Framework version 4.5.2 or higher to be present on the VM."
    service="microsoft.recoveryservices"
    resource="backup"
    authors="srinathvasireddy"
    ms.author="srinathvasireddy"
    displayOrder=""
    articleId="azurebackup-crc-usererrordotnetversionupgraderequired"
    diagnosticScenario="azurebackup-crc-usererrordotnetversionupgraderequired"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="15207"
    cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error UserErrorDotNetVersionUpgradeRequired

<!--issueDescription-->
We have identified that your backup configuration failed because of unsupported .NET version.
<!--/issueDescription-->

## **Recommended Steps**

To resolve this issue, perform the below:

- Ensure the .NET version matches the requirements listed [here](https://docs.microsoft.com/azure/backup/sql-support-matrix). If not, upgrade to latest version (this might require machine reboot).
- After upgrading and rebootin, retry the operation
