<properties
    pageTitle="Cluster's user password is expired"
    description="Cluster's user password is expired"
    infoBubbleText="Found recent cluster failure. See details on the right."
    service="microsoft.hdinsight"
    resource="clusters"
    authors="nealbh"
    ms.author="nebhatta"
    displayOrder="140"
    articleId="Hdi_PasswordExpired"
    diagnosticScenario="HDInsightUserPasswordExpiredInsight"
    selfHelpType="rca"
    supportTopicIds="32636421, 32636420"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_HDInsight"
/>

# We ran diagnostics on your resource and found an issue
<!--issueDescription-->
We noticed that the HDInsight cluster <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName--> has been failing due to an expired user password.
<!--/issueDescription-->

## **Recommended Steps**

* Please change your password in the Azure portal or on-premise, then wait for the password to update before retrying to log onto the cluster

<!--$users-->[users]<!--/$users--> 
