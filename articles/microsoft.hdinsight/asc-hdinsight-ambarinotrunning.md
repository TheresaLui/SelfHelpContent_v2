<properties
    ms.author="v-anreg"
    pageTitle="Ambari service not running"
    description="Ambari Service Issue"
    infoBubbleText="Ambari service is not running. See details on the right."
    service="microsoft.hdinsight"
    resource="clusters"
    authors="anirudhrege"
    displayOrder=""
    articleId="Hdi_Ambari_ServerNotRunning"
    diagnosticScenario="HDInsightAmbariServerNotRunningInsight"
    selfHelpType="diagnostics"
    supportTopicIds="32636419"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_HDInsight"
/>

# Ambari Service is not running

## We ran diagnostics on your resource and found an issue

<!--issueDescription-->
The HDInsight cluster <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName--> is not running Ambari server. Ambari server has to run on the **headnodehost** to display any metrics.
<!--/issueDescription-->

In an HDInsight cluster, the **headnodehost** is the default headnode on which Ambari server is started. All Ambari agents in the cluster will send heartbeats to the **headnodehost**.
Since the **headnodehost** is not running Ambari server, it cannot display the corresponding metrics correctly.

## **Recommended Steps**

1. You can connect to Ambari service using Secure Shell (SSH): `ssh \<clustername>\-ssh.azurehdinsight.net`
2. Run the following command to open host file /etc/host on one of the headnodes using Vi: `vi /etc/hosts/`
3. Look up for the headnode which has **headnodehost** mentioned next to it to verify that this headnode is the active node <br>
4. Run the following command to start Ambari service on the **headnodehost**: `sudo systemctl start ambari-server`

## **Recommended Documents**

* [Connect to HDInsight using SSH](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-linux-use-ssh-unix)
* [Manage HDInsight clusters by using the Ambari Web UI](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-manage-ambari)
