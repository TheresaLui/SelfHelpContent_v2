<properties
    pageTitle="databricks subnet full"
    description="Cluster unable to start due to subnet full."
    infoBubbleText="No Enough Public IP Address available due to subnet full. "
    service="microsoft.databricks"
    resource="workspaces"
    authors="nsarang"
    ms.author="nsarang"
    displayOrder=""
    articleId="Databricks_SubnetFull"
    diagnosticScenario="DatabricksSubnetFullInsight"
    selfHelpType="rca"
    supportTopicIds="32677649, 32677680, 32677678, 32677671, 32677670, 32677655"
    resourceTags=""
    productPesIds="16432"
    cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabricks"
/>

# We ran diagnostics on your resource and found the following issue
<!--issueDescription-->
Databricks Cluster deployed in <!--$Subnet-->Subnet<!--/$Subnet--> does not have sufficient free public IP addresses.
<!--/issueDescription-->

## **Recommended Steps**

In order to create space on the virtual network please perform following steps:

* Delete all clusters within the subnet
* [Change subnet settings](https://docs.microsoft.com/azure/virtual-network/virtual-network-manage-subnet#change-subnet-settings) to the existing virtual network to include a larger address space
* Create a new workspace with the updated subnet. Follow these [detailed migration](https://docs.microsoft.com/azure/azure-databricks/howto-regional-disaster-recovery#detailed-migration-steps) steps to copy resources (notebooks, cluster configurations, jobs) from the old to new workspace.

## **Recommended Documents**

* [Deploying Azure Databricks in your Azure Virtual Network](https://docs.azuredatabricks.net/administration-guide/cloud-configurations/azure/vnet-inject.html)
