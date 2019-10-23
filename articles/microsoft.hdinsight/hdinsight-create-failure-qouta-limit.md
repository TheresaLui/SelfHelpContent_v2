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
    cloudEnvironments="public"
    articleId="0a3f2d71-7001-4cf0-8591-a95d9b0ce136"
/>

# Create failure due to quota limit

## **Recommended Steps**

**Error: Code\":\"DeploymentQuotaExceeded\",\"Message\":\"Creating the deployment 'subDeployment-XX-XXXXXXXXXXXXXXXXXXXXXXXXXXXX' would exceed the quota of '800''**

Azure has a quota limit of 800 deployments per resource group. Quotas are applied per resource group, subscriptions, accounts, and other scopes. For example, your subscription may be configured to limit the number of cores for a region. If you attempt to deploy a virtual machine with more cores than the permitted amount, you receive an error stating the quota has been exceeded.

Solution:

1. Login to portal and click on HDInsights Clusters
2. Select your Cluster and on the Overview,  Tab Select the Resource Group Associated with that Cluster
3. Once you are in your Resource Group Select 'Deployments' 
4. Select and delete the deployments that are no longer needed


For more information, see [Resolve errors for resource quotas](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-quota-errors).

**Error: The maximum node exceeded the available cores in this region**

Your subscription may be configured to limit the number of cores for a region. If you attempt to deploy a resource with more cores than the permitted amount, you receive an error stating the quota has been exceeded.

To request a quota increase, follow these steps:

1. Go to Azure portal, and then select **Help + support**
2. Select **New support request**
3. On the **New support request** page, under **Basics** tab, select the following options:

    - Issue type: Service and subscription limits (quotas)
    - Subscription: the subscription you want to modify
    - Quota type: HDInsight

For more information, see [Create a support ticket to increase core](https://docs.microsoft.com/azure/hdinsight/hdinsight-capacity-planning#quotas).
