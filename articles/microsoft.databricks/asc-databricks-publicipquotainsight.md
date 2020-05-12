<properties
    pageTitle="Databricks Public IPAddress quota limit"
    description="Databricks cluster failure due to exceeding public ipaddress quota per resource group."
    infoBubbleText="Not enough Public IP Address available within Resource Group. "
    service="microsoft.databricks"
    resource="workspaces"
    authors="nsarang"
    ms.author="nsarang"
    displayOrder=""
    articleId="Databricks_PublicIPAddress_quotalimit"
    diagnosticScenario="DatabricksPublicIpQuotaInsight"
    selfHelpType="rca"
    supportTopicIds="32677649, 32677680, 32677678, 32677671, 32677670, 32677655"
    resourceTags=""
    productPesIds="16432"
    cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabricks"
/>

# We ran diagnostics on your resource and found the following issue
<!--issueDescription-->
Databricks Cluster scaling failed due to exceeding the quota of '800' resources per resource group:  **<!--$ManagedResourceGroupId-->[ManagedResourceGroupId]<!--/$ManagedResourceGroupId-->**. 
<!--/issueDescription-->

## **Recommended Steps**

If there is single cluster in a workspace:

* Delete existing cluster
* Re-deploy a new cluster with a bigger VM size

If there are multiple clusters in the same workspace: 

* Create a different workspace
* Move some of the jobs to new workspace

## **Recommended Documents**

* [Azure subscription and service limits, quotas, and constraints](https://docs.microsoft.com/azure/azure-subscription-service-limits#resource-group-limits)
* [Workspace Migration](https://docs.microsoft.com/azure/azure-databricks/howto-regional-disaster-recovery#detailed-migration-steps)
