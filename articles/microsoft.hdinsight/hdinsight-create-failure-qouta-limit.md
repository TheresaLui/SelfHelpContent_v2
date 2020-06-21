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

If your subscription requires a quota increase, click **Previous** and change the **Issue type** to **Service and subscription limits (quotas)** and then continue with your support request. For complete instructions, see [Create a support ticket to increase core](https://docs.microsoft.com/azure/hdinsight/quota-increase-request#gather-required-information). If you received the error "The maximum node exceeded the available cores in this region" that indicates your subscription requires a quota increase.

**To check available cores**

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


## **Recommended Documents**

* [Create Cluster Error Dictionary](https://docs.microsoft.com/azure/hdinsight/create-cluster-error-dictionary)
