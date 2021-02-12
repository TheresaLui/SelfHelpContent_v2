<properties
    pageTitle="Cluster failed due to Livy 2.1 error"
    description="Cluster failed due to Livy 2.1 error"
    infoBubbleText="Found recent cluster failure. See details on the right."
    service="microsoft.hdinsight"
    resource="clusters"
    authors="anirudhrege"
    ms.author="v-anreg"
    displayOrder=""
    articleId="Hdi_LivyError"
    diagnosticScenario="HDInsightLivyErrorInsight"
    selfHelpType="rca"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public, mooncake, blackforest, fairfax, usnat, ussec"
	ownershipId="AzureData_HDInsight"
/>

# We ran diagnostics on your resource and found an issue
<!--issueDescription-->
HDInsight cluster <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName--> failed due to Livy 2.1 error.
<!--/issueDescription-->

## **Recommended Steps**

The cluster creation failed with a legacy issue caused by Livy version 2.1. Retry will resolve the issue in some cases. Please wait at least 2 minutes before attempting to retrying cluster creation. If you would like to resolve this issue completely, use Spark 2.3 instead. 
