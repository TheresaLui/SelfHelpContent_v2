<properties
    pageTitle="Cluster Scaling Fails Due To Inaccessible Custom Script"
    description="Cluster Scaling Fails Due To Inaccessible Custom Script"
    infoBubbleText="Found recent cluster scale failure. See details on the right."
    service="microsoft.hdinsight"
    resource="clusters"
    authors="ansi12"
    displayOrder="23"
    articleId="Hdi_ScaleFailure_SasKeyExpired"
    selfHelpType="rca"
    supportTopicIds="32588504, 32511179"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, MoonCake"
/>

# We ran diagnostics on your resource and found an issue

## Problem

We noticed that the HDInsight cluster <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName--> has been failing a scale up operation. The failure is due to a persisted custom script that is inaccessible. This is because the script <!--$ScriptUri-->[ScriptUri]<!--/$ScriptUri--> uses a SAS key, which has expired.

## **Recommended steps**
In order to scale up, the persisted script needs to be demoted, so that it does not run on the new node.

There are 2 options to make persisted scripts work with scale ups:

1. To ensure that custom scripts work throughout the lifetime of the cluster, the [best practice](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-script-actions-linux#bPS2) is to store these scripts in the default storage account associated with the cluster. If this storage account is used, then there is no need to use a SAS key.

1. If you want to use a different storage account with a SAS key, then the script needs to be added again with a new SAS key. Keep in mind that this can fail again if the cluster is scaled up after the key expires.
