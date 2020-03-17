<properties
    pageTitle="Training clusters or Compute Instance hitting quota issues"
    description="Article on Amlcompute quota issues"
    service="microsoft.machinelearning"
    resource="Microsoft.MachineLearningServices/workspaces/computes"
    authors="nishankgu"
    ms.author="nigup"
    selfHelpType="generic"
    articleId="microsoft-machinelearning-amlcompute-quota.md"
    supportTopicIds="32690876"
    productPesIds="16644"
    cloudEnvironments="public, fairfax, mooncake"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# When you are hitting quota issues specific to Amlcompute

This helps users to understand quota, view usage and increase the quota for Amlcompute

## **Recommended Steps**

1. Quota is a limit that is enforced by Azure to prevent fraudulent subscriptions from using Azure capacity, and to control capacity overruns in a particular region. If you are creating a training cluster or a compute instance, they share the same quota and it is internal to Azure Machine Learning compute. Check if you have enough quota by going to the "Quotas + Usages" section in your workspace for the region you are experiencing this issue in.
2. It is also possible that your subscription owner has applied quota limits at your workspace level to better distribute capacity across various workspaces in your subscription. You may need to contact them to request an increase in the quota in that case.
3. If you have sufficient quota, it is possible that another cluster in your workspace is using the quota. Since quota is at a VM series level, and clusters or instances are specific to a VMSize it is possible that another cluster is sharing and using quota.

## **Recommended Documents**

* [Learn how to view your Azure Machine Learning quota](https://docs.microsoft.com/azure/machine-learning/how-to-manage-quotas#view-your-usage-and-quotas)
* [Understand how workspace level quotas work](https://docs.microsoft.com/azure/machine-learning/how-to-manage-quotas#workspace-level-quota)
