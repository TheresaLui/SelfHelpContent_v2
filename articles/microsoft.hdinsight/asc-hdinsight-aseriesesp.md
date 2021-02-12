<properties
    pageTitle="ESP cluster creation failure for A-series headnode size VM"
    description="Enterprise Security Package cluster creation fails for A-series headnode size VM"
    infoBubbleText="Found recent cluster failure. See details on the right."
    service="microsoft.hdinsight"
    resource="clusters"
    authors="anirudhrege"
    ms.author="v-anreg"
    displayOrder=""
    articleId="Hdi_ASeriesEsp_CreationFailure"
    diagnosticScenario="HDInsightASeriesEspClusterInsight"
    selfHelpType="rca"
    supportTopicIds="32636423, 32636488, 32681541"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, mooncake, blackforest, fairfax, usnat, ussec"
	ownershipId="AzureData_HDInsight"
/>

# We ran diagnostics on your resource and found an issue

<!--issueDescription-->
HDInsight cluster <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName--> creation is failing for A-series headnode size VM for Enterprise Security Package.
<!--/issueDescription-->

## **Recommended Steps**

* Create a cluster with Head node VM size D13_V2 or above
 
 
## **Recommended Documents**

* [Virtual machine sizes](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-provision-linux-clusters#virtual-machine-sizes)
