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
    cloudEnvironments="public, blackForest, fairfax, mooncake"
/>

# We ran diagnostics on your resource and found the following issue
<!--issueDescription-->
Ambari agent(s) for the following node(s) cannot send heartbeat: <!--$AlertHost-->[AlertHost]<!--/$AlertHost--> <br>
Ambari agents running on nodes send periodical heartbeat messages to let the server know that the node is running.
<!--/issueDescription-->

## **Recommended Steps**

There can be many possible root causes:

**1. Ambari Agent Not Started**

* You can connect to Ambari service using Secure Shell (SSH): `ssh <clustername>-ssh.azurehdinsight.net`
* Check if Ambari-agent is running: `service ambari-agent status`
* If not, check if failover controller services are running: `ps -ef | grep failover`
* If failover controller services are not running, check hdinsight-agent log: `/var/log/hdinsight-agent/hdinsight-agent.out`

**2. Ambari agent has high percentage CPU utilization**

* Run the following command to find process id of Ambari-agent: `ps -ef | grep ambari_agent`
* Then run the following command to show CPU utilization: `top -p <ambari-agent-pid>`
* Restart the Ambari-Agent if CPU utilization is high: `service ambari-agent restart`
* You can also try killing the Ambari Agent process and starting it again: `kill -9 <ambari-agent-pid>`, `service ambari-agent start`

**3. Networking Issue**

* Check if any of the /etc/hosts or /etc/resolv.conf files were manually modified

## **Recommended Documents**

* [Apache Ambari heartbeat issues in Azure HDInsight](https://docs.microsoft.com/azure/hdinsight/hadoop/apache-ambari-troubleshoot-heartbeat-issues)
