<properties
	pageTitle="Geo Replication, Failover Groups and DB Copy/Configuring or using failover groups"
	description="Geo Replication, Failover Groups and DB Copy/Configuring or using failover groups"
	service="microsoft.sql"
	resource="servers"
	authors="subbuk,maboja-msft"
	ms.author="subbuk,maboja"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32731230"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	articleId="a564aa55-abf9-41d1-96eb-2687717b4dab"
	ownershipId="AzureData_AzureSQLDB_Availability"
/>

# Geo Replication, Failover Groups and DB Copy/Configuring or using failover groups

## **Recommended Steps**

You can [Configure a failover group for Azure SQL DB](https://docs.microsoft.com/azure/sql-database/sql-database-configure-failover-group?WT.mc_id=pid:13491:sid:32731230/) from Azure Portal or using PowerShell. Before creating failover group(s), it is critical to ensure the server login and the firewall settings for the secondary server matches your primary server.

### **Failover group for Private link**

In order to use Private links with your failover group:

- Ensure your primary and secondary servers are in a paired region
- Create the virtual network and subnet in each region to host private endpoints for primary and secondary servers such that they have non-overlapping IP address spaces, e.g. the primary virtual network address range of 10.0.0.0/16 and the secondary virtual network address range of 10.0.0.1/16 overlaps
- Create a private endpoint and Azure Private DNS zone for the primary server
- Create a private endpoint for the secondary server as well, but this time choose to reuse the same Private DNS Zone that was created for the primary server
* Once the private link is established, start creating the failover group

### **Geo Replication and Failover groups**

- Removing a failover group for a single or pooled database does not stop replication, and it does not delete the replicated database
- You will need to manually stop geo-replication and delete the database from the secondary server if you want to add a single or pooled database back to a failover group after it's been removed
- Failing to do either of the above may result in an error similar to **"The operation cannot be performed due to multiple errors when attempting to add the database to the failover group"**

## **Recommended Documents**

* [Permissions Required to Manage  Failover group](https://docs.microsoft.com/azure/sql-database/sql-database-auto-failover-group?WT.mc_id=pid:13491:sid:32731230/)<br>
* [REST Api to Create/Update failover Group](https://docs.microsoft.com/rest/api/sql/failovergroups/createorupdate?WT.mc_id=pid:13491:sid:32731230/)   
