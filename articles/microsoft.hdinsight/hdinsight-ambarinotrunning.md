<properties
    authorAlias="v-anreg"
    pageTitle="Ambari service not running"
    description="AmbariPortalIssue"
    infoBubbleText="Ambari service is not running. See details on the right."
    service="microsoft.hdinsight"
    resource="clusters"
    authors="anirudhrege"
    displayOrder=""
    articleId="Hdi_Ambari_ServerNotRunning"
    diagnosticScenario="HDInsightAmbariServerNotRunningInsight"
    selfHelpType="diagnostics"
    supportTopicIds="32588422, 32588429, 32588445"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public"
/>

# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
The HDInsight cluster <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName--> is not running Ambari server.
Ambari server has to run on the **headnodehost** to display any metrics.
<!--/issueDescription-->

In an HDInsight cluster, the **headnodehost** is the default headnode on which ambari server is started. All Ambari agents in the cluster will send heartbeats to the **headnodehost**.
Since the **headnodehost** is not running ambari server, it cannot display the corresponding metrics correctly.

## **Recommended Steps**

1. Connect to Ambari service using Secure Shell (SSH).<br>
```	

		ssh <clustername>-ssh.azurehdinsight.net
```
2. Open host file /etc/host on one of the headnodes using Vi.<br>

```

		vi /etc/hosts/	
```
3. Look up for the headnode which has **headnodehost** mentioned next to it. This headnode is the active node.<br>

4. Start Ambari service on the **headnodehost**.<br>
```

		sudo ambari-server start
```

## **Recommended Documents**

* [Connect to HDInsight using SSH](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-linux-use-ssh-unix)
* [Manage HDInsight clusters by using the Ambari Web UI](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-manage-ambari)
