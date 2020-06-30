<properties
	pageTitle="create drop and manage resources/elastic job agents"
	description="create drop and manage resources/elastic job agents"
	service="microsoft.sql"
	resource="jobAgents"
	authors="joke"
    ms.author="joke"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32739626"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake,usnat,ussec"
	articleId="e8618d1e-0b04-18ee-1cb4-f6ab2326b027"
	ownershipId="AzureData_AzureSQLDB_Provisioning"
/>

# create drop and manage resources/elastic job agents

## **Recommended Steps**

* [Create and manage Elastic Job agents in Azure SQL Database](https://docs.microsoft.com/azure/sql-database/sql-database-elastic-pool-manage?WT.mc_id=pid:13491:sid:32630419/)
* If you are experiencing a restriction with creating Job agents and you are seeing an error similar to
`The Job agent could not be created because it would exceed the maximum Job agent quota of 5 for your subscription in the selected region`, 
feel free to continue creating this ticket as a request to bump up your Job agent quota.
* If you are experiencing Job step timeouts with your ongoing Job executions, make sure you try bumping up your job step's timeout values such as `step_timeout_seconds`, `retry_attempts`, and `retry_interval_backoff_multiplier`.
	* See [sp_update_jobstep](https://docs.microsoft.com/azure/azure-sql/database/elastic-jobs-tsql-create-manage#sp_update_jobstep) T-SQL documentation or [Set-AzSqlSqlElasticJobStep](https://docs.microsoft.com/powershell/module/az.sql/Set-AzSqlElasticJobStep) for PowerShell documentation for more details on how to update step retry or timeout settings for your Job step.
* If you are seeing an increase in your Job database storage size due to Job execution history taking up space, you can use the [sp_purge_job_history](https://docs.microsoft.com/azure/azure-sql/database/elastic-jobs-tsql-create-manage#delete-old-job-history) to cleanup more job history prior to a certain date. By default, the Jobs service retains job execution history of 45 days.

## **Recommended Documents**

* [Overview of Elastic Jobs](https://docs.microsoft.com/azure/sql-database/elastic-jobs-overview)
* [Elastic Jobs PowerShell documentation](https://docs.microsoft.com/azure/sql-database/elastic-jobs-powershell)
* [Elastic Jobs T-SQL documentation](https://docs.microsoft.com/azure/sql-database/elastic-jobs-tsql)

### Tutorials
* [Elastic Jobs in Azure SQL Database What and Why](https://techcommunity.microsoft.com/t5/azure-sql-database/elastic-jobs-in-azure-sql-database-what-and-why/ba-p/1177902)
* [Fundamental Concepts for Elastic Jobs in Azure SQL Database](https://techcommunity.microsoft.com/t5/azure-sql-database/fundamental-concepts-for-elastic-jobs-in-azure-sql-database/ba-p/1177939)
* [Creating an Elastic Jobs Agent, Credentials, and Jobs for Azure SQL Database in PowerShell](https://techcommunity.microsoft.com/t5/azure-sql-database/creating-an-elastic-jobs-agent-credentials-and-jobs-for-azure/ba-p/1179929)
* [Creating an Elastic Jobs Agent, Credentials, and Jobs for Azure SQL Database using T-SQL](https://techcommunity.microsoft.com/t5/azure-sql-database/creating-an-elastic-jobs-agent-credentials-and-jobs-for-azure/ba-p/1180096)
* [Running, Scheduling and Monitoring Elastic Jobs in Azure SQL Database](https://techcommunity.microsoft.com/t5/azure-sql-database/running-scheduling-and-monitoring-elastic-jobs-in-azure-sql/ba-p/1180179)
* [Troubleshooting Common issues with Elastic Jobs in Azure SQL Database](https://techcommunity.microsoft.com/t5/azure-sql-database/troubleshooting-common-issues-with-elastic-jobs-in-azure-sql/ba-p/1180766)

### REST API Documentation
* [Job Agents](https://docs.microsoft.com/rest/api/sql/jobagents)
* [Credentials](https://docs.microsoft.com/rest/api/sql/jobcredentials)
* [Target Groups](https://docs.microsoft.com/rest/api/sql/jobtargetgroups)
* [Jobs](https://docs.microsoft.com/rest/api/sql/jobs)
* [Job Steps](https://docs.microsoft.com/rest/api/sql/jobsteps)
* [Job Executions](https://docs.microsoft.com/rest/api/sql/jobexecutions)
* [Job Step Executions](https://docs.microsoft.com/rest/api/sql/jobstepexecutions)
* [Job Target Executions](https://docs.microsoft.com/rest/api/sql/jobtargetexecutions)