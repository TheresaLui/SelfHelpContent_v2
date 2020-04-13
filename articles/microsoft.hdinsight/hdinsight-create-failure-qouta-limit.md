<properties
    pageTitle="Create failure due to quota limit"
    description="Create failure due to quota limit"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="genlin"
    ms.author="jaserano"
    displayOrder=""
    selfHelpType="Generic"
    supportTopicIds="32681543"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="0a3f2d71-7001-4cf0-8591-a95d9b0ce136"
	ownershipId="AzureData_HDInsight"
/>

# Create failure due to quota limit

**Known issues**

As of March 18th, 2020 some Azure HDInsight customers have received error notifications when creating or scaling HDInsight clusters in some regions. Errors related to this issue include:

- Internal server error occurred while processing the request. Please retry the request or contact support.
- At least one resource deployment operation failed. Please list deployment operations for details. Please see https://aka.ms/DeployOperations for usage details
- User SubscriptionId '\<Subscription ID\>' does not have cores left to create resource '\<cluster name>'. Required: \<X\>, Available: 0.

Engineers are aware of this issue and are actively investigating.

For updates on the issue, see the Known Issues section of the [Release Notes](https://docs.microsoft.com/en-us/azure/hdinsight/hdinsight-release-notes#known-issues) page.

For additional help, continue creating this support request.

## **Recommended Steps**

To check the cores available to the cluster, do the following steps:

1. Navigate to the **Overview** page for the HDInsight cluster
2. On the left menu, click **Quota limits**

   The page displays the number of cores in use, the number of available cores, and the total cores.

**Error: Code\":\"DeploymentQuotaExceeded\",\"Message\":\"Creating the deployment 'subDeployment-XX-XXXXXXXXXXXXXXXXXXXXXXXXXXXX' would exceed the quota of '800''**

Azure has a quota limit of 800 deployments per resource group. Quotas are applied per resource group, subscriptions, accounts, and other scopes. For example, your subscription may be configured to limit the number of cores for a region. If you attempt to deploy a virtual machine with more cores than the permitted amount, you receive an error stating the quota has been exceeded.

Solution:

1. In the Azure portal, navigate to the HDInsight overview page for the cluster
2. Click the resource group link
3. On the Resource Group page, on the left menu, click **Deployments**
4. Select and delete the deployments that are no longer needed

For more information, see [Resolve errors for resource quotas](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-quota-errors).

**Error: The maximum node exceeded the available cores in this region**

Your subscription may be configured to limit the number of cores for a region. If you attempt to deploy a resource with more cores than the permitted amount, you receive an error stating the quota has been exceeded.

To request a quota increase, follow these steps:

1. Go to Azure portal, and then select **Help + support**
2. Select **New support request**
3. On the **New support request** page, under **Basics** tab, select the following options:

    - Issue type: Service and subscription limits (quotas)
    - Subscription: the subscription you want to modify
    - Quota type: HDInsight

For more information, see [Create a support ticket to increase core](https://docs.microsoft.com/azure/hdinsight/hdinsight-capacity-planning#quotas).
