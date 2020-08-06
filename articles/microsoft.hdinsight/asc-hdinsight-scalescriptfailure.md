<properties
    pageTitle="Cluster Scaling Fails Due To Inaccessible Custom Script"
    description="Cluster Scaling Fails Due To Inaccessible Custom Script"
    infoBubbleText="Found recent cluster scale failure. See details on the right."
    service="microsoft.hdinsight"
    resource="clusters"
    authors="ansi12"
    ms.author="ansiva"
    displayOrder="23"
    articleId="Hdi_ScaleFailure_SasKeyExpired"
    diagnosticScenario="HDInsightCustomizationInsight"
    selfHelpType="rca"
    supportTopicIds="32681537"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_HDInsight"
/>

# We ran diagnostics on your resource and found an issue
<!--issueDescription-->
We noticed that the HDInsight cluster <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName--> has been failing a scale up operation. The failure is due to persisted custom scripts that are inaccessible. The following scripts use an expired SAS key:

 <!--$ScriptUri-->[ScriptUri]<!--/$ScriptUri-->
<!--/issueDescription-->

## **Recommended Steps**

In order to scale up, the persisted script needs to be demoted so it does not run on the new node. There are 2 options to make persisted scripts work with scale ups:

1. To ensure that custom scripts work throughout the lifetime of the cluster, the [best practice](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-script-actions-linux#bPS2) is to store these scripts in the default storage account associated with the cluster. If this storage account is used, then there is no need to use a SAS key.
1. If you want to use a different storage account with a SAS key, then the script needs to be added again with a new SAS key. Keep in mind that this can fail again if the cluster is scaled up after the key expires.

## **Recommended Documents**

* [Storage shared access signatures (SAS) overview](https://docs.microsoft.com/azure/storage/common/storage-sas-overview)
