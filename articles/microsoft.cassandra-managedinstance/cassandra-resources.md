<properties
	pageTitle="Azure Managed Instance Apache Cassandra resources"
	description="Azure Managed Instance Apache Cassandra resources"
	service="microsoft.cassandra"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32788355,32788363,32788359"
	resourceTags=""
	productPesIds="17480"
    cloudEnvironments="public,fairfax,blackforest,mooncake,usnat,ussec"
	articleId="cassandra-resources"
	displayOrder="40"
	category="Cluster"
	ownershipId="AzureData_AzureManagedInstanceCassandra"
/>

# Azure Managed Instance Apache Cassandra resources
Most users are able to resolve their Managed Instance Cassandra resources issue using the steps below.

## **Recommended Steps**

### **Creating a cluster fails**

Creating a cluster fails
- Verify if you are creating the cluster in a supported region
- Verify the Azure Cosmos DB Network Contributor has permission on the subnet (see https://docs.microsoft.com/azure/network-watcher/required-rbac-permissions)
- Verify the subscription has the expected quota/permissions


## **Recommended Documents**
[FAQ for Azure Managed Instance Apache Cassandra](https://docs.microsoft.com/azure/managed-instance-apache-cassandra/faq)