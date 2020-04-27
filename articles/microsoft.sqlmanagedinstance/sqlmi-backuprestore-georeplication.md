<properties
	pageTitle="Business Continuity|Geo-replication"
	description="Business Continuity|Geo-replication"
	service="microsoft.sql"
	resource="servers"
	authors="jovanpop-msft"
    ms.author="jovanpop"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32637264,32637263"
	productPesIds="16259"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	articleId="4640a2ab-ec5e-4a0a-8946-fe6524807455"
	ownershipId="AzureData_AzureSQLMI"
/>

# Geo replication (Preview)

Geo-replication in Managed Instance enables you to automatically replicate your changes to another region using [Auto failover groups](https://docs.microsoft.com/azure/sql-database/sql-database-auto-failover-group). Note that this feature is still in preview and has some known issues.

## **Recommended Steps**

Try some of the following steps to troubleshoot the issue:

- If you want to configure [active geo-replication](https://docs.microsoft.com/azure/sql-database/sql-database-active-geo-replication) note that this feature is not available in Managed Instance. You must use [Auto failover groups](https://docs.microsoft.com/azure/sql-database/sql-database-auto-failover-group).
- If you are trying to configure [Auto failover groups](https://docs.microsoft.com/azure/sql-database/sql-database-auto-failover-group) to multiple regions, this feature is not supported in Managed Instance. Currently, you can use only one region for geo-replication.
- If the connection between primary and secondary Managed Instances cannot be established, check are the resources in secondary VNet reachable from the primary VNets. You would need to use express route or Gateway to connect the networks, and to remove any firewall rules that can block the traffic.
- If the VNets are connected check are you using [Global VNet peering](https://docs.microsoft.com/azure/virtual-network/virtual-networks-faq#what-are-the-constraints-related-to-global-vnet-peering-and-load-balancers). VNet peering is not supported in Geo-replication scenario and you need to use express route or Gateway to connect the VNets
- If you are getting the error in while you are trying to change service tier (change cores or storage, or move from General Purpose to Business Critical or vice versa), this operation is currently not supported.
- Check are there some [known issues or limitations](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-transact-sql-information) such as transactional replication don't work with Geo-replication.

## **Recommended Documents**

- [Best practices for configuring Geo-replication in Managed Instance](https://docs.microsoft.com/azure/sql-database/sql-database-auto-failover-group#best-practices-of-using-failover-groups-with-managed-instances) 
- [Disaster recovery using database geo-replication](https://docs.microsoft.com/azure/sql-database/saas-dbpertenant-dr-geo-replication?WT.mc_id=pid:13491:sid:32630424/)