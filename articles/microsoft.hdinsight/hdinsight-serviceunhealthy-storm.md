<properties
    pageTitle="Storm: Troubleshooting"
    description="Azure HDInsight Storm Troubleshooting"
    service="microsoft.hdinsight"
    resource="clusters"
    authors="TobyTu"
    ms.author="jaserano"
    displayOrder=""
    selfHelpType="Generic"
    supportTopicIds="32636503"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="fe94f714-8472-9562-8b07-b1cbbe1d922a"
	ownershipId="AzureData_HDInsight"
/>

# Azure HDInsight Storm Troubleshooting

**Reboot your nodes.** If your node is unresponsiveness and/or you see that some services have not started, reboot the VMs using PowerShell or Rest API following the steps in the article [Reboot VMs for HDInsight cluster](https://docs.microsoft.com/azure/hdinsight/cluster-reboot-vm).

**Locating Storm binaries and configuration files**. Storm binaries are located at `/usr/hdp/current/storm-client`. Storm Log4J configuration is read from `usr/hdp/storm/log4j2`.

## **Recommended Documents**

* [Troubleshoot Apache Storm on Azure HDInsight](https://docs.microsoft.com/azure/hdinsight/storm/apache-troubleshoot-storm)
* [Storm Binaries location](https://hdinsight.github.io/storm/storm-binaries-location.html)
* [Storm Log4J Configuration location](https://hdinsight.github.io/storm/storm-log4j-configuration.html)
* [Storm EventHub Spout binaries](https://hdinsight.github.io/storm/storm-eventhub-spout-landing.html)
* [Ambari agent heartbeat lost Alert](https://hdinsight.github.io/ambari/ambari-agent-heartbeat-lost.html)
