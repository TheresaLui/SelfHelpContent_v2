<properties
	pageTitle="Availability Group Failure, Failover, Sync issue"
	description="Availability Group Failure, Failover, Sync issue"
	infoBubbleText="Availability Group Failure, Failover, Sync issue"
	service="Microsoft.SqlVirtualMachine"
	resource="SqlVirtualMachines"
	ms.author="ujpat,amamun,babarmav"	
	authors="ujpat,amamun,babarmav"
	displayOrder="1"
	diagnosticScenario=""
	selfHelpType="diagnostics"
	supportTopicIds="32740064"
	resourceTags="windowsSQL"
	productPesIds="14745,16342"
	cloudEnvironments="public,fairfax, usnat, ussec, blackforest, mooncake"
	articleId="ae736c5e-fff3-4eb1-9368-1711f998ccba"
	ownershipId="AzureData_AzureSQLVM"
/>

# We ran diagnostics on your resource and found the below steps which can help you. 
<!--issueDescription--> 

Most users can resolve issues concerning **How do I setup AG** by using the following steps.

<!--/issueDescription--> 
 
## **Recommended Steps** 

**[Compare different ways](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-overview#deployment)** to setup AG and follow any of the following methods that suits you
  * Manual Process:
      * Step 1 - [configure Availability Group Pre-requisites](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-manually-configure-prerequisites-tutorial) 
      * Step 2-   [Always on Configuration-Manually](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-manually-configure-tutorial)
  * [Use PowerShell or Az CLI to configure an availability group](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-az-commandline-configure?tabs=azure-cli)
  * [Use Azure Quick-start templates to configure an availability group](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-quickstart-template-configure)
  * [Configure Availability Group Using Azure Portal-Preview](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-azure-portal-configure?tabs=azure-cli)
  
## **Recommended Documents**
- [Monitor and Troubleshoot](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/always-on-availability-groups-troubleshooting-and-monitoring-guide?view=sql-server-ver15&WT.mc_id=Portal-Microsoft_Azure_Support) Availability Groups
- [Monitor performance](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/monitor-performance-for-always-on-availability-groups?view=sql-server-ver15) for Always On availability groups
- Troubleshoot: Availability group exceeded [RPO](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/troubleshoot-availability-group-exceeded-rpo?view=sql-server-ver15) or [RTO](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/troubleshoot-availability-group-exceeded-rto?view=sql-server-ver15)
- [Changes from primary replica are not reflected](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/troubleshoot-primary-changes-not-reflected-on-secondary?view=sql-server-ver15) on secondary
- [Useful tools](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/useful-tools-for-troubleshooting?view=sql-server-ver15) for AG troubleshooting
- [Recommendations for Index Maintenance](https://techcommunity.microsoft.com/t5/sql-server-support/recommendations-for-index-maintenance-with-alwayson-availability/ba-p/318518) with Availability Groups
