<properties
    pageTitle="Quota issues while creating or scaling up a cluster or an instance"
    description="Article on quota issues seen while creating compute"
    service="microsoft.machinelearning"
    resource="Microsoft.MachineLearningServices/workspaces/computes"
    authors="nishankgu"
    ms.author="nigup"
    selfHelpType="generic"
    articleId="microsoft-machinelearning-quota-issues.md"
    supportTopicIds="32690873"
    productPesIds="16644"
    cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# When you are facing quota issues while creating any type of compute in Azure Machine Learning

This helps users to understand quota, view usage and increase the quota for various types of compute when using Azure Machine Learning

## **Recommended Steps**

1. Quota is a limit that is enforced by Azure to prevent fraudulent subscriptions from using Azure capacity, and to control capacity overruns in a particular region. If you are creating an AKS cluster, it uses the all-up subscription level quota to limit the number of cores on such type of clusters. 
2. If you are creating a training cluster or a compute instance, they share the same quota and it is internal to Azure Machine Learning compute. Check if you have enough quota by going to the "Quotas + Usages" section in your workspace for the region you are experiencing this issue in.
3. It is also possible that your subscription owner has applied quota limits at your workspace level to better distribute capacity across various workspaces in your subscription. You may need to contact them to request an increase in the quota in that case.

## **Recommended Documents**

* [Learn how to view your all-up subscription quota](https://docs.microsoft.com/azure/virtual-machines/windows/quotas)
* [Learn how to view your Azure Machine Learning quota](https://docs.microsoft.com/azure/machine-learning/how-to-manage-quotas#view-your-usage-and-quotas)
* [Understand how workspace level quotas work](https://docs.microsoft.com/azure/machine-learning/how-to-manage-quotas#workspace-level-quota)
