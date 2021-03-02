<properties
	pageTitle="Azure Managed Instance Apache Cassandra resources"
	description="Azure Managed Instance Apache Cassandra resources"
	service="microsoft.documentdb"
	resource="cassandraClusters"
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
Most users can resolve issues with Managed Instance Cassandra resources using the steps below.

## **Recommended Steps**

### **Creating a cluster fails**

- Verify if you are creating the cluster in a supported region
- Verify that the Azure Cosmos DB Network Contributor has permission on the subnet. See [required RBAC permissions](https://docs.microsoft.com/azure/network-watcher/required-rbac-permissions).
- Verify that the subscription has the expected quota/permissions

## **Recommended Documents**
[FAQ for Azure Managed Instance Apache Cassandra](https://docs.microsoft.com/azure/managed-instance-apache-cassandra/faq)
