<properties
	pageTitle="application/backupandrestore"
	description="application/backupandrestore"
	service="microsoft.servicefabric"
	resource="clusters"
	authors="chiragpa"
    ms.author="chiragpa"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32608941"
	resourceTags=""
	productPesIds="15842"
	cloudEnvironments="public"
	articleId="8c3b1732-d9ec-4dd9-bbe9-23d722436c2b"
/>

# application/backupandrestore

## Active Known Issue with Service Fabric Linux Clusters 
A recent update introduced an issue for Service Fabric Linux clusters where Ubuntu based Service Fabric nodes will be unable to do core management operations unless the dependent package is downgraded to the previous version (2.3.4-4). 

**Impacted Customers:** This will affect all customers running Azure Service Fabric Linux clusters.

## **Recommended Steps**
A script is available to help mitigate the issue. This needs to be applied as a Custom Script Extension to your ARM (Azure Resource Manager) template.

For detailed mitigation steps and support resources please see this [post](https://blogs.msdn.microsoft.com/azureservicefabric/2019/02/07/known-issue-for-service-fabric-linux-clusters/). 

## **Recommended Documents**

* [Service Fabric Backup and Restore](https://docs.microsoft.com/azure/service-fabric/service-fabric-reliable-services-backup-restore)<br>
* [Configure Periodic backup for Azure Cluster](https://docs.microsoft.com/azure/service-fabric/service-fabric-backuprestoreservice-quickstart-azurecluster)<br>
* [Configure Periodic backup for Standalone Cluster](https://docs.microsoft.com/azure/service-fabric/service-fabric-backuprestoreservice-quickstart-standalonecluster)<br>
