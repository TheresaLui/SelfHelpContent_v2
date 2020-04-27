<properties
    pageTitle="HDInsight CRUD failure with invalid VM SKU"
    description="HDInsight CRUD failure with invalid VM SKU"
    infoBubbleText="Found recent invalid vm SKU error. See details on the right."
    service="microsoft.hdinsight"
    resource="clusters"
    authors="nealbh"
    ms.author="nebhatta"
    displayOrder=""
    articleId="Hdi_InvalidVmSeries"
    diagnosticScenario="HDInsightInvalidVmSeriesInsight"
    selfHelpType="rca"
    supportTopicIds="32636423"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_HDInsight"
/>

# We ran diagnostics on your resource and found the following issue
<!--issueDescription-->
There is a problem creating HDInsight cluster <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName--> because there is an invalid virtual machine SKU.
<!--/issueDescription-->

## **Recommended Steps**

* Please update the virtual machine SKU to one of the SKUs mentioned here : <!--$ErrorDescription-->[ErrorDescription]<!--/$ErrorDescription--> 

## **Recommended Documents**

* [Azure HDInsight G-series VMs deprecation](https://azure.microsoft.com/updates/azure-hdinsight-g-series-deprecation-plan/)
 
