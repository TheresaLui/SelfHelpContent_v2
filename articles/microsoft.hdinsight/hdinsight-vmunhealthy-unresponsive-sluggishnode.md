<properties
    pageTitle="Troubleshooting unhealthy nodes or VMs"
    description="TSG / How-to for know scenario"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="ramakoni1"
    ms.author="ramakoni"
    displayOrder=""
    selfHelpType="Generic"
    supportTopicIds="32636481"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
    articleId="hdinsight-vmunhealthy_responsive_sluggishnode"
	ownershipId="AzureData_HDInsight"
/>
# Unresponsive or sluggish node in a cluster

## **Recommended Steps**

* **Reboot your nodes.** If your node is unresponsiveness and/or you see that some services have not started, reboot the VMs using PowerShell or Rest API following the steps in the article [Reboot VMs for HDInsight cluster](https://docs.microsoft.com/azure/hdinsight/cluster-reboot-vm).
* **Check for low disk space.** In some cases, sluggishness can occur because of low disk space on the cluster. To check for this issue, follow these steps:

1. SSH into each of the nodes, and check disk usage on the node by running a command such as the following:
 
   > -df -h

   > -du -h --max-depth=1 / | sort -h
 
1. Review the command output, and check for the presence of any large files in the mnt folder or other folders. Typically, the resource, usercache, and appcache (mnt/resource/hadoop/yarn/local/usercache/hive/appcache/) folders contain these kinds of large files. 
1. If there are large files, this indicates that either a current job is causing the file growth or a failed previous job may have contributed to this issue. To check whether this behavior is caused by a current job, run the following command: `-sudo du -h --max-depth=1 /mnt/resource/hadoop/yarn/local/usercache/hive/appcache/`
1. If this command indicates a specific job, you can choose to terminate the job by using a command that resembles the following: `-yarn application -kill application_`<appid>`. If no specific jobs are indicated, go to the next step.
1. After the command in step 4 completes, and if no specific jobs are indicated, delete the files that you found in step 2 by running a command that resembles the following: `-rm -rf filecache usercache`

NOTE: If you have large files that you want to keep but that are contributing to the low disk space issue, you have to scale up your HDInsight cluster and restart your services.

After you complete this procedure and wait for a few minutes, you will notice that the storage is freed up and the node’s usual performance is restored.

## **Recommended Documents**

* [Troubleshoot: Ambari agent heartbeat lost issue](https://hdinsight.github.io/ambari/ambari-agent-heartbeat-lost.html)
* [Troubleshoot a slow or failing HDInsight cluster](https://docs.microsoft.com/azure/hdinsight/hdinsight-troubleshoot-failed-cluster)
