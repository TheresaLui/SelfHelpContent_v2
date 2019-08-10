<properties
    pageTitle="HDInsight Create Cluster Error when Service Bypass Disabled"
    description="HDInsightServiceBypassDisabled"
    infoBubbleText="Cluster Creation Error When Service Bypass Disabled. See details on the right."
    service="microsoft.hdinsight"
    resource="clusters"
    authors="RaviChitturi"
    ms.author="v-ravikc"
    displayOrder=""
    articleId="Hdi_ServiceBypassDisabled"
    diagnosticScenario="HDInsightServiceBypassDisabledInsight"
    selfHelpType="rca"
    supportTopicIds="32636423, 32636439, 32636444"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public"
/>

# We ran diagnostics on your resource and found the following issue

## Problem
There is a problem while creating a HDInsight cluster <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName--> because Service Bypass is disabled.

Since "Allow trusted Microsoft services to access <!--$StorageAccount-->[StorageAccount]<!--/$StorageAccount-->storage account checkbox is not checked" unable to create a cluster

## **Recommended Steps**

1. Go to the Storage Account that was selected during the cluster creation
2. Select the Firewalls and Virtual networks in the left pane in Azure Portal
3. Then select the Selected networks radio button
4. Check the "Allow trusted Microsoft services to access <!--$StorageAccount-->[StorageAccount]<!--/$StorageAccount-->storage account" checkbox

## **Recommended Documents**

* [Service Bypass is disabled](https://docs.microsoft.com/en-us/azure/hdinsight/hdinsight-hadoop-use-blob-storage)
