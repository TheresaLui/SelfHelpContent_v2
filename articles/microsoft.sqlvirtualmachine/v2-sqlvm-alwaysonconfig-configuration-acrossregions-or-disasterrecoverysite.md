<properties
	pageTitle="AlwaysOn Availability Groups - Configuration - Across Regions Or Disaster Recovery Site"
	description="AlwaysOn Availability Groups - Configuration - Across Regions Or Disaster Recovery Site"
	infoBubbleText="AlwaysOn Availability Groups - Configuration - Across Regions Or Disaster Recovery Site"
	service="Microsoft.SqlVirtualMachine"
	resource="SqlVirtualMachines"
	ms.author="ujpat"	
	authors="ujpat"
	displayOrder="1"
	diagnosticScenario=""
	selfHelpType="diagnostics"
	supportTopicIds="32740063"
	resourceTags="windowsSQL"
	productPesIds="14745,16342"
	cloudEnvironments="public,fairfax, usnat, ussec, blackforest, mooncake"
	articleId="d32972ca-a4e3-4130-814a-be40c84f5f7e"
	ownershipId="AzureData_AzureSQLVM"
/>

# We ran diagnostics on your resource and found the below steps which can help you. 
 

<!--issueDescription--> 

Most users can resolve issues **configuring Availability Group across different regions or as a Disaster Recovery Site** by using the following information.


<!--/issueDescription--> 


## **Recommended Steps** 

* **Configure Availability Group across different regions or as a Disaster Recovery Site** 

  You already have or are planning to create an Availability Group between two nodes. You're planning to set up the third node on Azure to extend your on-premises environment or your Azure AG environment. See [Configure a SQL Server Always On availability group across different Azure regions](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-manually-configure-multiple-regions) to set up the Disaster Recovery Site. 
 

* **Things to Keep in Mind when Configuring Multi-Region, Always On Availability Groups** 
 
  - If your Availability Group spans across Azure and on-premises (a hybrid environment), you will still need a load balancer. If you are using SQL 2019 CU8+ on Windows 2016, you can [use DNN](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-distributed-network-name-dnn-listener-configure) instead of a load balancer/ 

   - Update the client connection strings to set **MultiSubnetFailover=Yes** for [Fast failovers and avoiding Application Timeouts](https://docs.microsoft.com/sql/relational-databases/native-client/features/sql-server-native-client-support-for-high-availability-disaster-recovery?view=sql-server-ver15#connecting-with-multisubnetfailover) 
 
  - Make sure you have tuned your [Failover cluster Network Thresholds](https://docs.microsoft.com/windows-server/troubleshoot/iaas-sql-failover-cluster#recommendations-for-changing-to-more-relaxed-settings-for-multi-tenant-environments-like-azure-iaas) to a higher value to avoid failovers. 
	

## **Recommended Documents** 

* [Failover to Remote Region or DR Site](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/availability-group-manually-configure-multiple-regions#fail-over-to-remote-region) 
* [Prerequisites, Restrictions, and Recommendations for Always On availability groups](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/prereqs-restrictions-recommendations-always-on-availability?view=sql-server-ver15) 
* [Add a Replica to Always On](https://docs.microsoft.com/sql/database-engine/availability-groups/windows/use-the-add-replica-to-availability-group-wizard-sql-server-management-studio?view=sql-server-ver15) 

