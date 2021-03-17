<properties
	pageTitle="create drop and manage resources/ARM template issues or questions"
	description="create drop and manage resources/ARM template issues or questions"
	service="microsoft.sql"
	resource="servers"
	authors="emlisa,andikshi"
    ms.author="emlisa,andikshi"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32630406"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	articleId="820cb442-f2b2-41df-af4f-86beefabd56f"
	ownershipId="AzureData_AzureSQLDB_Provisioning"
/>

# create drop and manage resources/ARM template issues or questions

For Azure SQL Database and Azure SQL Managed Instance, Azure Resource Manager (ARM) templates help you define your infrastructure as code and deploy your solutions to the Azure cloud.

* [List of available templates for Azure SQL Database](https://docs.microsoft.com/azure/azure-sql/database/arm-templates-content-guide?tabs=single-database)

## Troubleshoot deployment issues 

From Azure Resource Manager, examine specific operations in past deployments that used templates to see which resources were deployed. This history also contains information about any errors.

* [View Deployment History](https://docs.microsoft.com/azure/azure-resource-manager/templates/deployment-history?tabs=azure-portal)
* [Troubleshoot common deployment errors with ARM](https://docs.microsoft.com/azure/azure-resource-manager/templates/common-deployment-errors)

### Look up resource types that had issues

If your ARM template deployment runs into an issue with any of the following resource types: re-select your problem type / problem sub type to get help faster.
| Type                                                  | Problem Type             | Problem SubType
| ----------------------------------------------------- | ------------------------ | ------------------------ |
| Microsoft.Sql/servers                                 | Create or Drop Resources | Servers                  |
| Microsoft.Sql/servers/databases                       | Create or Drop Resources | Databases                |
| Microsoft.Sql/servers/elasticPools                    | Create or Drop Resources | Elastic Pools            |
| Microsoft.Sql/servers/firewallRules                   | Create or Drop Resources | Firewall Rules           |
| Microsoft.Sql/servers/jobAgents                       | Create or Drop Resources | Elastic job or job agent |
| Microsoft.Sql/servers/auditingSettings                | Security, Privacy and Compliance | Auditing |
| Microsoft.Sql/servers/azureADOnlyAuthentications      | Security, Privacy and Compliance | Azure Active Directory authentication |
| Microsoft.Sql/servers/keys                            | Security, Privacy and Compliance | TDE and Customer Managed Key (CMK)    |
| Microsoft.Sql/servers/encryptionProtector             | Security, Privacy and Compliance | Always Encrypted |
| Microsoft.Sql/servers/vulnerabilityAssessments        | Security, Privacy and Compliance | Vulnerability Assessment |
| Microsoft.Sql/servers/privateEndpointConnections      | Connectivity: Configuration and How-To Questions | Private Link |
| Microsoft.Sql/servers/virtualNetworkRules             | Connectivity: Configuration and How-To Questions | Network settings, TCP ports and firewalls |
| Microsoft.Sql/servers/backupLongTermRetentionVaults   | Backup and Restore | Long-term backup retention |
| Microsoft.Sql/servers/syncAgents                      | BACPAC, Data Sync and Replication | SQL Data Sync |
| Microsoft.Sql/servers/failoverGroups                  | Geo Replication, Failover Groups and DB Copy | Configuring or using failover groups |

## **Recommended Documents**

* [Debugging ARM template deployments](https://azure.microsoft.com/blog/debugging-arm-template-deployments?WT.mc_id=pid:13491:sid:32630406/)
