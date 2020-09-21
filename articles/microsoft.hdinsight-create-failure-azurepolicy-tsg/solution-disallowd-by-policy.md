<properties
	pageTitle="RequestDisallowedByPolicy"
	description="RequestDisallowedByPolicy"
    service="Microsoft.HDInsight"
    resource="Microsoft.HDInsight/clusters"
	authors="Jacky-hdi"
	ms.author="linjzhu"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="b9100f52-3a30-42d8-a7e6-1c26dc83c6c5"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# RequestDisallowedByPolicy

<!--issueDescription-->

We have checked the cluster and it seems that cluster creation failure is due to below azure policy

***{paste policy name here}***

<!--/issueDescription-->


To resolve the issue:
1. Please follow the recommended documents to check Azure policy
2. If conflict, please remove this policy and retry to create the cluster again



## **Recommended Documents**

* [Resource Policy Restrictions](https://docs.microsoft.com/en-us/azure/hdinsight/hadoop/hdinsight-troubleshoot-cluster-creation-fails#resource-policy-restrictionss)
* [Azure Policy Overview](https://docs.microsoft.com/en-us/azure/governance/policy/overview)

