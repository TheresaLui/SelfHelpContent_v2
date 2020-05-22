<properties
    pageTitle="Databricks throttling for workspace"
    description="Databricks cluster throttling issue per subscription."
    infoBubbleText="Databricks cluster scaling failing due to throttling per subscription. "
    service="microsoft.databricks"
    resource="workspaces"
    authors="nsarang"
    ms.author="nsarang"
    displayOrder=""
    articleId="Databricks_Cluster_Throttling"
    diagnosticScenario="DatabricksClusterThrottlingInsight"
    selfHelpType="rca"
    supportTopicIds="32677649, 32677680, 32677678, 32677671, 32677670, 32677681, 32677655"
    resourceTags=""
    productPesIds="16432"
    cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabricks"
/>

# We ran diagnostics on your resource and found the following issue
<!--issueDescription-->
The workspace **<!--$ResourceName-->ResourceName<!--/$ResourceName-->** has been throttled at least **<!--$ThrottledRequests-->ThrottledRequests<!--/$ThrottledRequests-->** times, while performing '<!--$OperationName-->OperationName<!--/$OperationName-->' during cluster autoscale (Scale up and Scale down).
<!--/issueDescription-->

## **Recommended Steps**

Operations : **'<!--$OperationName-->OperationName<!--/$OperationName-->'** has exceeded subscription limits.

* Identify list of ARM API failures from Azure Support Center -> Resource Explorer's Event Tab
* Please ask Customer to stop all the jobs and wait until all jobs are stopped
* Restart Jobs

## **Recommended Documents**

* [Troubleshooting API throttling errors](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshooting-throttling-errors)
* [Throttling Resource Manager requests](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-request-limits)
