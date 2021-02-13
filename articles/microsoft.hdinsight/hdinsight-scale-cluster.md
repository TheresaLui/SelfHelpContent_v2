<properties
    pageTitle="Scale HDInsight Cluster"
    description="How to for know scenario"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="mimig1"
    ms.author="mimig"
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

**Cluster is unresponsive during or after scaling**

If your node is unresponsive and/or you see that some services have not started, reboot the VMs using PowerShell or Rest API by following the steps to [reboot VMs for HDInsight cluster](https://docs.microsoft.com/azure/hdinsight/cluster-reboot-vm).

**YARN UI not accessible after scale-down**

Node label information is stored in the `nodelabel.mirror` file, which is stored in HDFS. If replication = 1, then this file only has one replica. During a cluster scale-down, if the node that stores this file is deleted and this file is not backed up on the remaining nodes, YARN will not be able to find available nodes to assign tasks.

You can resolve this issue by using the following steps:

1. Increase the replication factor to 3 (a one-time operation) by running the following command:

```
hadoop fs -setrep -R  3 hdfs://mycluster:8020/yarn/node-labels
```
2. Disabling Node label from Ambari

**Error: Code":"DeploymentQuotaExceeded","Message":"Creating the deployment 'subDeployment-XX-XXXXXXXXXXXXXXXXXXXXXXXXXXXX' would exceed the quota of '800**

Azure has a quota limit of 800 deployments per resource group. Scale deployments will fail when the limit is reached. Because the customer's HDInsight cluster resource resides in their resource group, in their resource subscription, and the actual cluster assets reside in our provisioning subscriptions in its own resource group, this issue can happen when the limit is reached in either of the resource groups.

1. From Azure Portal, sign into the portal and navigate to your resource group
1. Select **Deployments** from the resource group. If this count shows that it has reached the limit, delete old deployments to fix the issue. You can safely delete all deployments that are "X" days old. "X" can be 30 days or another number of days, based on how frequently deployments happen in this resource group.

**Operations Management Suite (OMS) is enabled and blocking the ability to scale**

Customers have experienced issues with scale-up operations failing during an OMS script installation. This is a known issue. If you have OMS enabled, disable OMS temporarily, scale up the cluster, then re-enable OMS.

To temporarily disable Operations Management Suite (OMS). use the following steps:

1. Log in to the Azure Portal. In the top search bar, search for HDInsight Cluster
1. Select the cluster that you want to scale
1. Scroll down to the Monitoring section and select **Operations Management Suite**
1. Select **Disable**, then click **Save**
1. After saving, then scale the cluster, and then re-enable OMS

**Additional Information**

* You can enable auto-scale only when creating a cluster. If you have not configured auto-scale when creating a cluster, you must delete the cluster, and create a new cluster with auto-scale enabled.
* HDInsight does not allow you to upgrade worker node disk sizes on a running cluster. Currently, you must choose the disk size when the cluster is created. HDInsight clusters are designed to be easily dropped and re-created.
* After a cluster is deployed, you cannot increase or decrease the diskspace of the nodes. You can free up logs or free data on mount to get more disk space.
* Head nodes cannot be scaled up. If you need additional head nodes, re-create your cluster with the number of head nodes required.
* We recommend that you scale down HDInsight to a minimum of three worker nodes. For Kafka, you cannot scale down the worker nodes.
* Scaling your HDInsight is not possible via ARM templates. You can scale your cluster by using one of the following five methods:
    * PowerShell Az
    * PowerShell AzureRM
    * Azure CLI
    * Azure Classic CLI
    * Azure portal

## **Recommended Documents**

* [Scale HDInsight clusters](https://docs.microsoft.com/azure/hdinsight/hdinsight-scaling-best-practices)
* [Custom Script Actions Troubleshooting](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-customize-cluster-linux#troubleshooting)
* [FAQ:Creating or deleting HDInsight clusters](https://docs.microsoft.com/azure/hdinsight/hdinsight-faq#creating-or-deleting-hdinsight-clusters)
