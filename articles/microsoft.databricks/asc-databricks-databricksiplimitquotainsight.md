<properties
    pageTitle="Databricks Public IP Count limit reached"
    description="Databricks cluster auto scale failed due to exceeding public IP limit."
    infoBubbleText="Not enough Public IP Address available within subscription. "
    service="microsoft.databricks"
    resource="workspaces"
    authors="nsarang"
    ms.author="nsarang"
    displayOrder=""
    articleId="Databricks_Crud_publicIplimit"
    diagnosticScenario="DatabricksIPLimitQuotaInsight"
    selfHelpType="rca"
    supportTopicIds="32677649, 32677680, 32677678, 32677671, 32677670, 32677655, 32677702"
    resourceTags=""
    productPesIds="16432"
    cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabricks"
/>

# We ran diagnostics on your resource and found the following issue
<!--issueDescription-->
Databricks cluster auto scale failed due to **<!--$Message-->[Message]<!--/$Message-->**. Operation Failed: **<!--$Count-->[Count]<!--/$Count-->**
<!--/issueDescription-->

## **Recommended Steps**

Databricks clusters use one public IP address per node. If your subscription ID: <!--$SubscriptionId-->[SubscriptionId]<!--/$SubscriptionId--> has already used all its public IPs, you should request to increase the quota:

* Please raise a [ticket](https://portal.azure.com/#blade/Microsoft_Azure_Support/HelpAndSupportBlade/overview)
* Select Issue type "Service and subscription limits(quotas)"
* Select Subscription ID <!--$SubscriptionId-->[SubscriptionId]<!--/$SubscriptionId-->
* Select Quota type "Networking" and hit next button to navigate "Details" tab
* Click on "Provider details" link
* Select "Resource Manager" as Deployment Model and Location for increasing quota limit
* Select "Public IP Addresses" as Resources and provide new limits of public addresses
* Review request details and click create button for raising request for increasing quota limit

## **Recommended Documents**

* [Azure subscription and service limits, quotas, and constraints](https://docs.microsoft.com/azure/azure-subscription-service-limits#resource-group-limits)
* [Resource Manager Quota Request](https://docs.microsoft.com/azure/azure-supportability/resource-manager-core-quotas-request)
