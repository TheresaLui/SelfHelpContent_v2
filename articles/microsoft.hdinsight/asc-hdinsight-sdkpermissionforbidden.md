<properties
    pageTitle="HDInsight SDK Permission Forbidden"
    description="HDInsight - User Subscription 403 Forbidden Errors"
    infoBubbleText="User is getting 403 permission error, due to change in role-based accesses. See details on the right."
    service="microsoft.hdinsight"
    resource="clusters"
    authors="shawnawei"
    ms.author="xunwei"
    displayOrder="157"
    articleId="Hdi_SdkPermissionForbidden"
    diagnosticScenario="HDInsightSdkPermissionForbiddenInsight"
    selfHelpType="rca"
    supportTopicIds="32636455"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public, blackforest, mooncake, fairfax, usnat, ussec"
	ownershipId="AzureData_HDInsight"
/>

# We ran diagnostics on your resource and found the following issue
<!--issueDescription-->
We determined that the HDInsight cluster <!--$ClusterDnsName-->[ClusterDnsName]<!--/$ClusterDnsName--> configurations are now behind granular role-based access control and require the Microsoft.HDInsight/clusters/configurations/* permission to access them.
<!--/issueDescription-->

## **Recommended Steps**
To obtain this permission, assign the HDInsight Cluster Operator, Contributor, or Owner role to the user <!--$Username-->[Username]<!--/$Username--> or service principal trying to access configurations.

## **Recommended Documents**

* [Why am I seeing a 403 (Forbidden) response after updating my API requests and/or tool?](https://docs.microsoft.com/azure/hdinsight/hdinsight-migrate-granular-access-cluster-configurations#faq)

