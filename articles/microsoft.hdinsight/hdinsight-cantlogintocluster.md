<properties
    pageTitle="I can't log in to my cluster"
    description="I can't log in to my cluster"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="mimig1"
    ms.author="mimig"
    displayOrder=""
    selfHelpType="Generic"
    supportTopicIds="32636506"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public,mooncake, Fairfax, usnat, ussec, blackForest"
    articleId="a03309d2-a1c2-4d5d-b068-fa2ff15f5fa8"
	ownershipId="AzureData_HDInsight"
/>

# I can't log in to my cluster

## **Recommended Steps**

To resolve common issues, try one or more of the following steps.  Keep in mind that when logging in to the cluster or app dashboards, you must use your cluster login or HTTP credentials. When connecting remotely, use your Secure Shell (SSH) or Remote Desktop credentials.

* **Reboot your nodes.** If your node is unresponsive and/or you see that some services have not started, reboot the VMs using PowerShell or Rest API following [these steps](https://docs.microsoft.com/azure/hdinsight/cluster-reboot-vm).
* **Reset login password.** To reset the cluster login password, click **Reset Credential** in the [SSH + Cluster login](data-blade:Microsoft_Azure_HDInsight.LinuxLoginSettingBlade) tab.
* **Reset credentials from Ambari.** For Linux clusters, if you forget your SSH credentials, you can [reset the credentials within the Ambari UI](https://azure.microsoft.com/documentation/articles/hdinsight-administer-use-portal-linux/#change-passwords).
* **Review your SSH logs.** Review your SSH logs can help to troubleshoot your issue. To review your logs, use the following command:

```
ssh -vvv sshuser@-ssh.azurehdinsight.net
```
* **Review blocked ports.** Ensure that there are no port blocks on ports 22 and 23. To SSH into a cluster, these ports must be accessible. For more information, see [Connect to HDInsight (Apache Hadoop) using SSH](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-linux-use-ssh-unix).

## **Recommended Documents**

* [Manage clusters in the portal - Change login password](https://azure.microsoft.com/documentation/articles/hdinsight-administer-use-portal-linux/#change-passwords)<br>
* [Connect to HDInsight (Apache Hadoop) using SSH](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-linux-use-ssh-unix)<br>
* [Azure Security Baseline for HDInsight](https://docs.microsoft.com/azure/hdinsight/security-baseline)
