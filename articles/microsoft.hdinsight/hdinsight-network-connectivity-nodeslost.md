<properties
    pageTitle="HDInsight cluster node connectivity lost"
    description="HDInsight cluster node connectivity lost"
    infoBubbleText="One or more nodes failed to respond to the ping. Please check the details."
    service="microsoft.hdinsight"
    resource="clusters"
    authors="maha-arun"
    displayOrder="29"
    articleId="Hdi_NetworkConnectivity_NodeLost"
    diagnosticScenario="HDInsightNetworkConnectivityInsight"
    selfHelpType="diagnostics"
    supportTopicIds="32588427"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public"
/>

# We ran diagnostics on your resource and found an issue

## Problem

 We pinged all the nodes in your HDInsight cluster <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName--> and the nodes listed below consistently failed to respond.

### Failing nodes
<!--$FailedNodeInformation-->[FailedNodeInformation]<!--/$FailedNodeInformation-->

## **Recommended steps**
 To start troubleshooting this connectivity failure with the nodes, we need the following log files from the failing nodes. Run the following commands to collect and compress the logs to home directory and send the compressed files to the support professional.

1. tar czvf ~/syslog.tgz /var/log/syslog*
2. tar czvf ~/kernlog.tgz /var/log/kern.log*
3. tar czvf ~/auth.tgz /var/log/auth.log* 
4. tar czvf ~/ambari.tgz /var/log/ambari-*