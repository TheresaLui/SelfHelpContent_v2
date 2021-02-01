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

We have checked the cluster. It seems that cluster creation failure is due to the following Azure policy.

***{paste policy name here}***

<!--/issueDescription-->

**Recommended Steps**

1. Review the following recommended documents to check Azure policy
2. If a conflict results, remove the policy and try to create the cluster again

## **Recommended Documents**

* [RequestDisallowedByPolicy](https://docs.microsoft.com/en-us/azure/hdinsight/create-cluster-error-dictionary#error-code-deployments-failed-due-to-policy-violation-resource--was-disallowed-by-policy-policy-identifiers-policyassignmentname-idprovidersmicrosoftmanagementmanagementgroups-providersmicrosoftauthorizationpolicyassignmentspolicydefinition-)
* [Resource Policy Restrictions](https://docs.microsoft.com/en-us/azure/hdinsight/hadoop/hdinsight-troubleshoot-cluster-creation-fails#resource-policy-restrictionss)
* [Azure Policy Overview](https://docs.microsoft.com/en-us/azure/governance/policy/overview)

