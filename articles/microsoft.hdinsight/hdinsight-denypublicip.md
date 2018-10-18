<properties
    pageTitle="HDInsight failure due to public poliy in place denying public IP creation"
    description="HDInsight failure due to public poliy in place denying public IP creation"
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

## Problem

Creation of the HDInsight cluster <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName--> failed because the there is a public policy in place to deny the creation of public IPs. HDInsight cluster creation requires two public IPs in order for creation to be successful.

## **Recommended steps**
Modify the public policy <!--$policyDefinitionName-->[policyDefinitionName]<!--/$policyDefinitionName--> to allow public IP creation and trigger a cluster creation deployment.