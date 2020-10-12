<properties
    pageTitle="Databricks Cores quota limitation"
    description="Insufficient cores within subscription."
    infoBubbleText="No cores available within subscription. See details on the right."
    service="microsoft.databricks"
    resource="workspaces"
    authors="nsarang"
    ms.author="nsarang"
    displayOrder=""
    articleId="Databricks_Crud_quotalimit"
    diagnosticScenario="DatabricksCoresQuotaInsight"
    selfHelpType="rca"
    supportTopicIds="32677649, 32677680, 32677678, 32677671, 32677670, 32677681, 32677655"
    resourceTags=""
    productPesIds="16432"
    cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabricks"
/>

# We ran diagnostics on your resource and found the following issue
<!--issueDescription-->
Cluster unable to start/scale due to insufficient number of cores within the subscription: <!--$SubscriptionId-->[SubscriptionId]<!--/$SubscriptionId-->

Current number of cores in use: <!--$CurrentDeploymentCount-->[CurrentDeploymentCount]<!--/$CurrentDeploymentCount-->

Maximum allowed cores: <!--$MaxAllowedQuota-->[MaxAllowedQuota]<!--/$MaxAllowedQuota-->

Requested cores: <!--$AdditionalRequestCores-->[AdditionalRequestCores]<!--/$AdditionalRequestCores-->

<!--/issueDescription-->

## **Recommended Steps**

* Check whether sufficient quota of cores are available in region for this subscription: <!--$SubscriptionId-->[SubscriptionId]<!--/$SubscriptionId-->

* Please follow instructions for raising a [ticket](https://docs.microsoft.com/azure/azure-supportability/per-vm-quota-requests) for more cores

## **Recommended Documents**

* [Handling Azure Resource Manager Deployment Limits](https://azure.microsoft.com/blog/azure-limits-quotas-increase-requests/)
* [Quota increase requests](https://docs.microsoft.com/azure/azure-supportability/resource-manager-core-quotas-request/)
* [GPU Family](https://docs.microsoft.com/azure/virtual-machines/linux/sizes-gpu/)
* [Cores available by region](https://azure.microsoft.com/global-infrastructure/services/?products=virtual-machines&regions=all/)
