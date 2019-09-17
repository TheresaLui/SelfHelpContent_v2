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
    cloudEnvironments="public"
/>

# We ran diagnostics on your resource and found the following issue
<!--issueDescription-->
Cluster unable to start/scale due to insufficient number of cores within the subscription. Requested Cores: <!--$AdditionalRequestCores-->[AdditionalRequestCores]<!--/$AdditionalRequestCores-->. 
<!--/issueDescription-->

## **Recommended Steps**

Please check whether sufficient quota of cores are available in region for this subscriptions <!--$Subscription Name-->[SubscriptionName]<!--/$Subscription Name-->

### Not enough cores available

1. Please follow instructions for raising a [ticket](https://docs.microsoft.com/azure/azure-supportability/regional-quota-requests#request-total-regional-vcpus-quota-increase-at-subscription-level-using-the-usages--quota-blade) 

## **Recommended Documents**

* [Handling Azure Resource Manager Deployment Limits](https://azure.microsoft.com/blog/azure-limits-quotas-increase-requests/)
* [Quota increase requests](https://docs.microsoft.com/azure/azure-supportability/resource-manager-core-quotas-request/)
* [GPU Family](https://docs.microsoft.com/azure/virtual-machines/linux/sizes-gpu/)
* [Cores available by region](https://azure.microsoft.com/global-infrastructure/services/?products=virtual-machines&regions=all/)
