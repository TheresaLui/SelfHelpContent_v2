<properties
    pageTitle="Cluster failure due to expired ADLS certificate"
    description="Cluster failure due to expired ADLS certificate"
    infoBubbleText="Found recent cluster failure. See details on the right."
    service="microsoft.hdinsight"
    resource="clusters"
    authors="anirudhrege"
    ms.author="v-anreg"
    displayOrder="26"
    articleId="Hdi_CertExpired"
    diagnosticScenario="HDInsightExpiredCertificateInsight"
    selfHelpType="rca"
    supportTopicIds="32636418, 32636420, 32636425"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_HDInsight"
/>

# We ran diagnostics on your resource and found an issue

## Problem
<!--issueDescription-->
The HDInsight cluster <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName--> is configured to use only Azure Data Lake Storage (ADLS) as storage which is accessed via a certificate. This certificate has expired and must be refreshed in order to access storage.
<!--/issueDescription-->

## Thumbprint of expired certificates
<!--$Thumbprint-->[Thumbprint]<!--/$Thumbprint-->

## **Recommended Steps**

1. Update the [ADLS certificate](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-use-data-lake-store#refresh-the-hdinsight-certificate-for-data-lake-storage-gen1-access) 
