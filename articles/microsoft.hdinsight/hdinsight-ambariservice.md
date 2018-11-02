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
The HDInsight cluster <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName--> has Ambari service running on both headnodes <!--$Host-->[Host]<!--/$Host-->
<!--/issueDescription-->

All Ambari agents in the cluster will send heartbeats to the server ‘headnodehost’ defined in /etc/ambari-agent/conf/ambari-agent.ini

'headnodehost' is the default headnode on which ambari server is started.

This is the reason why the Ambari server running on ‘headnodehost’ can receive heartbeats from all machines and display the corresponding metrics correctly while the Ambari server running on other headnode cannot receive those metrics.



## **Recommended steps**

* Open host file /etc/host on one of the headnodes using Vi

	~~ vi /etc/hosts/ ~~

* Look up for headnodehost, next to the FQDN of the headnode to note the active node.

* Browse to Ambari portal, to stop the service on the standby node.
