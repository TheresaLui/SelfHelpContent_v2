<properties
	pageTitle="Insufficient MI permission"
	description="Insufficient MI permission"
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
	articleId="e811b4dd-a437-4496-a272-926f82ee1d6e"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Insufficient MI permission

<!--issueDescription-->

We have checked the cluster and it seems that ESP cluster creation failure is due to insufficient MI permissions.

<!--/issueDescription-->

## **Recommended Steps**

1. Please follow the recommended documents to assign **HDInsight Domain Services Contributor** role to your managed identity 
2. Delete error cluster and recreate ESP cluster<br>

## **Recommended Documents**

* [Authorize a managed identity](https://docs.microsoft.com/azure/hdinsight/domain-joined/apache-domain-joined-configure-using-azure-adds#create-and-authorize-a-managed-identity)
