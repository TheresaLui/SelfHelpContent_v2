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
    cloudEnvironments="public"
/>

# We ran diagnostics on your resource and found the following issue
<!--issueDescription-->
The workspace <!--$ResourceName-->ResourceName<!--/$ResourceName--> has been throttled at least <!--$ThrottledRequests-->ThrottledRequests<!--/$ThrottledRequests--> times for <!--$OperationName-->OperationName<!--/$OperationName--> during cluster autoscale (Scale up and Scale down)
<!--/issueDescription-->

## **Recommended Steps**

Service Throttling  happens if you have exceeded subscription limits for <!--$OperationName-->OperationName<!--/$OperationName-->:

* Identify list of ARM API failures from Azure Support Center -> Resource Explorer's Event Tab. Databricks Control plane makes continuous retries in case of failures (VM Creation/Deletion).
* Please ask Customer to stop all the jobs and wait until all jobs are stopped. 
* Restart Jobs freshly from the beginning.

## **Recommended Documents**

* [Troubleshooting API throttling errors](https://docs.microsoft.com/en-us/azure/virtual-machines/troubleshooting/troubleshooting-throttling-errors)
* [Throttling Resource Manager requests](https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-request-limits)
