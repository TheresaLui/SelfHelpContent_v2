<properties
    pageTitle="HDInsight failure due to wasb secure transfer enabled"
    description="HDInsight failure due to wasb secure transfer enabled"
    infoBubbleText="Found recent cluster failure. See details on the right."
    service="microsoft.hdinsight"
    resource="clusters"
    authors="nealbh"
    ms.author="nebhatta"
    displayOrder="154"
    articleId="Hdi_WASB_Storage"
    diagnosticScenario="HDInsightWasbSecureTransferInsight"
    selfHelpType="rca"
    supportTopicIds="32636430"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_HDInsight"
/>

# We ran diagnostics on your resource and found the following issue
<!--issueDescription-->
We determined that the HDInsight cluster <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName--> has a WASB storage account with secure transfer enabled breaking the cluster.
<!--/issueDescription-->

## **Recommended Steps**

### **Determine the affected storage account**

1. Navigate to your cluster in the Azure portal
2. On the left side, within the Settings section, click Storage accounts
3. One of the storage accounts listed is your primary storage account

### **Disabling secure transfer**

1. Within the Azure portal search for your storage account, determined from the previous step 
2. On the left side, within the Setting section, click Configuration
3. Toggle Secure transfer required to disabled and save the configuration
4. Confirm that Ambari restarted any stopped services
