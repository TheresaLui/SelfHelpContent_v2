<properties
    pageTitle="HDInsight failure due to policy in place denying public IP creation"
    description="HDInsight failure due to policy in place denying public IP creation"
    infoBubbleText="Found recent cluster failure. See details on the right."
    service="microsoft.hdinsight"
    resource="clusters"
    authors="nealbh"
    ms.author="nebhatta"
    displayOrder="31"
    articleId="Hdi_Crud_PublicPolicy"
    diagnosticScenario="HDInsightDenyPublicIpInsight"
    selfHelpType="rca"
    supportTopicIds="32636423, 32636507"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_HDInsight"
/>

# We ran diagnostics on your resource and found the following issue
<!--issueDescription-->
We determined that creation of the HDInsight cluster <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName--> failed because there is a public policy in place to deny the creation of public IPs. HDInsight cluster creation requires two public IPs.
<!--/issueDescription-->

## **Recommended Steps**

* Please remove the policy <!--$policyDefinitionName-->[policyDefinitionName]<!--/$policyDefinitionName--> to allow public IP creation and then reattempt creation of the HDInsight cluster. The policy can be populated after cluster creation.

## **Recommended Documents** 

* [Create and manage policies](https://docs.microsoft.com/azure/governance/policy/tutorials/create-and-manage)
