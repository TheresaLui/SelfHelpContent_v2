<properties
	pageTitle="Insufficient MI permission"
	description="Insufficient MI permission"
	service=""
	resource=""
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

We have checked the cluster and it seems that ESP cluster creation failure is due to insufficient MI permission<br>
<br>
To resolve the issue:<br>
<br>
1. Please follow the recommended documents to assign **HDInsight Domain Services Contributor** role to your managed identity  <br>
2. Delete error cluster and recreate ESP cluster<br>

<!--/issueDescription-->

## Recommended documents

1. [Authorize a managed identity](https://docs.microsoft.com/azure/hdinsight/domain-joined/apache-domain-joined-configure-using-azure-adds#create-and-authorize-a-managed-identity)
