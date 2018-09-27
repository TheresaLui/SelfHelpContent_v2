<properties
    pageTitle="Cluster failure due to expired ADLS certificate"
    description="Cluster failure due to expired ADLS certificate"
    infoBubbleText="Found recent cluster failure. See details on the right."
    service="microsoft.hdinsight"
    resource="clusters"
    authors="nealbh"
    displayOrder="26"
    articleId="Hdi_CertExpired"
    diagnosticScenario="HDInsightRefreshCertificateInsight"
    selfHelpType="rca"
    supportTopicIds="32588501"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public"
/>

# We ran diagnostics on your resource and found an issue

## Problem

The HDInsight cluster <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName--> is configured to use only ADLS as storage which is accessed via a certificate. This certificate has expired and needs to be refreshed in order to access storage.

## Thumbprint of expired certificates
<!--$Details-->[Details]<!--/$Details-->

## **Recommended steps**
1. Update the [ADLS certificate](https://docs.microsoft.com/azure/hdinsight/hdinsight-hadoop-use-data-lake-store?toc=%2Fen-us%2Fazure%2Fhdinsight%2Fhadoop%2FTOC.json&bc=%2Fen-us%2Fazure%2Fbread%2Ftoc.json#refresh-the-hdinsight-certificate-for-data-lake-store-access) 

1. Restart the gateway node for the new certificate to take into effect