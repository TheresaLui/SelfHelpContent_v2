<properties
    pageTitle="Scale HDInsight Cluster"
    description="How to for know scenario"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="genlin"
    ms.author="jaserano"
    displayOrder=""
    selfHelpType="Generic"
    supportTopicIds="32681540,32681539"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="hdinsight-scale-cluster"
	ownershipId="AzureData_HDInsight"
/>
# Scale HDInsight Cluster

The following are the most common issues encountered when scaling HDInsight.

**Error: Code":"DeploymentQuotaExceeded","Message":"Creating the deployment 'subDeployment-XX-XXXXXXXXXXXXXXXXXXXXXXXXXXXX' would exceed the quota of '800**

Azure has a quota limit of 800 deployments per resource group. Scale deployments will fail when we hit this limit. Since the customer's HDInsight cluster resource resides in their resource group, in their resource subscription, and the actual cluster assets reside in our provisioning subscriptions in its own resource group, the issue can happen when we hit the limit in either of the resource groups.

1. From the portal, sign into the portal and navigate to your resource group
1. Select **Deployments** from the resource group. If this count shows that it has reached the limit, delete old deployments to fix the issue. You can safely delete all deployments that are "X" days old. "X" can be 30 or so based on how frequent deployments happen in this resource group.


**Operations Management Suite (OMS) is enabled and blocking the ability to scale**

Customers have experienced issues with scale-up operations failing during an OMS script installation. This is a known issue. If you have OMS enabled, please disable OMS temporarily, scale-up the cluster, then re-enable OMS.

To temporarily disable Operations Management Suite (OMS) follow steps below:

1. Login to the Azure Portal and in the top search bar search for HDInsight Cluster
1. Select the cluster you are looking to scale
1. Scroll down to the Monitoring section and select Operations Management Suite
1. Select disable then save
1. Once this is saved scale the cluster then re-enable OMS

**Additional Information**

* HDInsight does not allow you to upgrade worker node disk sizes on a running cluster. Currently, you must choose the disk size when the cluster is created. HDInsight clusters are designed to be easily dropped and re-created.
* Once a cluster is deployed, customer’s cannot increase or decrease the diskspace of the nodes. Customer’s can free up logs or free data on mount to get more disk space.
* It is recommended that you scale down HDInsight to a minimum of three worker nodes. For Kafka, you cannot scale down the worker nodes.
* Scaling your HDInsight is not possible via ARM templates. You can scale your cluster using five different methods:

    * PowerShell Az
    * PowerShell AzureRM
    * Azure CLI
    * Azure Classic CLI
    * Azure portal

* Customers can enable auto-scale only during when creating a cluster. If you have not configured auto-scale when creating a cluster, you must delete the cluster, and create a new cluster with auto-scale enabled.

## **Recommended Documents**

* [Scale HDInsight clusters](https://docs.microsoft.com/azure/hdinsight/hdinsight-scaling-best-practices)
* [Custom Script Actions Troubleshooting](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-customize-cluster-linux#troubleshooting)
* [FAQ:Creating or deleting HDInsight clusters](https://docs.microsoft.com/azure/hdinsight/hdinsight-faq#creating-or-deleting-hdinsight-clusters)
