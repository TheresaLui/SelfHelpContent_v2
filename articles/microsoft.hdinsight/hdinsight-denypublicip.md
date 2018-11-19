<properties
    pageTitle="HDInsight failure due to policy in place denying public IP creation"
    description="HDInsight failure due to policy in place denying public IP creation"
    infoBubbleText="Found recent cluster failure. See details on the right."
    service="microsoft.hdinsight"
    resource="clusters"
    authors="nealbh"
    displayOrder="31"
    articleId="Hdi_Crud_PublicPolicy"
    diagnosticScenario="HDInsightDenyPublicIpInsight"
    selfHelpType="rca"
    supportTopicIds="32588502, 32511166"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public"
/>

# We ran diagnostics on your resource and found the following issue

We determined that creation of the HDInsight cluster <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName--> failed because there is a public policy in place to deny the creation of public IPs. HDInsight cluster creation requires two public IPs.

## **Recommended steps**
Please remove the policy <!--$policyDefinitionName-->[policyDefinitionName]<!--/$policyDefinitionName--> to allow public IP creation and then reattempt creation of the HDInsight cluster. The policy can be populated after cluster creation.

## Further reading
Please refer to this [create and manage policies](https://docs.microsoft.com/azure/governance/policy/tutorials/create-and-manage) article for more information regarding subscription level policies.