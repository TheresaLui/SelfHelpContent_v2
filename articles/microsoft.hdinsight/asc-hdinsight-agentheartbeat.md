<properties
    pageTitle="Ambari agent heartbeat lost issue"
    description="Ambari agent is not sending heartbeat"
    infoBubbleText="Found recent agent heartbeat loss issue. See details on the right."
    service="microsoft.hdinsight"
    resource="clusters"
    authors="anirudhrege"
    ms.author="v-anreg"
    displayOrder=""
    articleId="Hdi_Ambari_AgentHeartbeatLoss"
    diagnosticScenario="HDInsightAgentNotSendingHeartbeatInsight"
    selfHelpType="rca"
    supportTopicIds="32636418, 32636430"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_HDInsight"
/>

# We ran diagnostics on your resource and found the following issue
<!--issueDescription-->
Ambari agent(s) for the following node(s) cannot send heartbeat: <!--$AlertHost-->[AlertHost]<!--/$AlertHost--> <br>
Ambari agents running on nodes send periodical heartbeat messages to let the server know that the node is running.
<!--/issueDescription-->

## **Recommended Documents**

* [Apache Ambari heartbeat issues in Azure HDInsight](https://docs.microsoft.com/azure/hdinsight/hadoop/apache-ambari-troubleshoot-heartbeat-issues)
