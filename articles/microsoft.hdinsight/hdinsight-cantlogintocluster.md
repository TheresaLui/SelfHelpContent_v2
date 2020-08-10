<properties
    pageTitle="I can't log in to my cluster"
    description="I can't log in to my cluster"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="bharathsreenivas"
    ms.author="jaserano"
    displayOrder=""
    selfHelpType="Generic"
    supportTopicIds="32636506"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public,mooncake, Fairfax"
    articleId="a03309d2-a1c2-4d5d-b068-fa2ff15f5fa8"
	ownershipId="AzureData_HDInsight"
/>

# I can't log in to my cluster

## **Recommended Steps**
To resolve common issues, try one or more of the following steps.  Keep in mind that when logging in to the cluster or app dashboards, use your "cluster login" or "HTTP" credentials. When connecting remotely, use your Secure Shell (SSH) or Remote Desktop credentials.

* **Reboot your nodes.** If your node is unresponsiveness and/or you see that some services have not started, reboot the VMs using PowerShell or Rest API following the steps in the article [Reboot VMs for HDInsight cluster](https://docs.microsoft.com/azure/hdinsight/cluster-reboot-vm).
* **Reset login password.** To reset the cluster login password, use the "Reset Credential" button in the [SSH + Cluster login](data-blade:Microsoft_Azure_HDInsight.LinuxLoginSettingBlade) tab.
* **Reset credentials from Abmari.** For Linux clusters, if you cannot recall your SSH credentials, you can [reset the credentials within the Ambari UI](https://azure.microsoft.com/documentation/articles/hdinsight-administer-use-portal-linux/#change-passwords).
 
Please ensure that there are no port blocks on ports 22 and 23. In order to SSH into a cluster these ports needs to be accessible. For more information [click here](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-linux-use-ssh-unix).

## **Recommended Documents**

* [Manage clusters in the portal - Change login password](https://azure.microsoft.com/documentation/articles/hdinsight-administer-use-portal-linux/#change-passwords)<br>
* [Connect to HDInsight (Apache Hadoop) using SSH](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-linux-use-ssh-unix)<br>
