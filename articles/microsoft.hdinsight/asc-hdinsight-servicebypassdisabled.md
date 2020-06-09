<properties
    pageTitle="HDInsight Service Bypass is disabled"
    Description="Cluster creation error as service bypass is disabled"
    infoBubbleText="Found recent cluster failure. See details on the right."
    service="microsoft.hdinsight"
    resource="clusters"
    authors="Ravi"
    ms.author="v-ravikc"
    displayOrder=""
    articleId="Hdi_ServiceBypassDisabled"
    diagnosticScenario="HDInsightServiceBypassDisabledInsight"
    selfHelpType="rca"
    supportTopicIds="32636423, 32636439, 32636444"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_HDInsight"
/>

# We ran diagnostics on your resource and found the following issue
<!--issueDescription-->
There is a problem while creating HDInsight cluster <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName--> because Service Bypass is disabled.

HDInsight deployment failed since "Allow trusted Microsoft services to access storage account <!--$StorageAccount-->[StorageAccount]<!--/$StorageAccount--> checkbox is not checked"
<!--/issueDescription-->

## **Recommended Steps**

1. Go to the Storage Account <!--$StorageAccount-->[StorageAccount]<!--/$StorageAccount--> that was selected during the cluster creation
2. Select the Firewalls and Virtual networks in the left pane in Azure Portal
3. Then select the Selected networks radio button
4. Check the "Allow trusted Microsoft services to access this storage account" checkbox in Exceptions

## **Recommended Documents**

* [Use Azure storage with Azure HDInsight clusters](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-use-blob-storage)
