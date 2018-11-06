<properties
    pageTitle="Ambari service running on both headnodes"
    description="AmbariPortalIssue"
    infoBubbleText="Ambari service is running on both headnodes. See details on the right."
    service="microsoft.hdinsight"
    resource="clusters"
    authors="anirudhrege"
    displayOrder=""
    articleId="Hdi_Ambari_ServiceRunningOnBothHeadnodes"
    diagnosticScenario="HDInsightAmbariServiceInsight"
    selfHelpType="diagnostics"
    supportTopicIds="32588422, 32588429, 32588445"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public"
/>

# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
The HDInsight cluster <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName--> has Ambari server running on both headnodes: <!--$Host-->[Host]<!--/$Host-->
Ambari server running on the headnode other than the **headnodehost** will not display any metrics on the Ambari portal.
<!--/issueDescription-->

In an HDInsight cluster, the **headnodehost** is the default headnode on which ambari server is started. All Ambari agents in the cluster will send heartbeats to only one headnode which is the **headnodehost**.
Since the **headnodehost** is receiving heartbeats from all machines, it can display the corresponding metrics correctly. Other instances of the Ambari server running on the other headnode cannot receive the heartbeats, thus they cannot display the metrics.

## **Recommended Steps**

1. Connect to Ambari service using Secure Shell (SSH).<br>
```	

		ssh <clustername>-ssh.azurehdinsight.net
		
```

2. Open host file /etc/host on one of the headnodes using Vi.<br>
```

		vi /etc/hosts/
		
```

3. Look up for the headnode which has **headnodehost** mentioned next to it. This headnode is the active node. The other headnode which does not have **headnodehost** mentioned is the standby node.

4. Stop Ambari service on the standby node.<br>
```

		sudo ambari-server stop
		
```

## **Recommended Documents**

* [Connect to HDInsight using SSH](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-linux-use-ssh-unix)
* [Manage HDInsight clusters by using the Ambari Web UI](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-manage-ambari)
