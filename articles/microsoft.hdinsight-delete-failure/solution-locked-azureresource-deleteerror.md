<properties
	pageTitle="Locked AzureResource DeleteError"
	description="Locked AzureResource DeleteError"
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
	articleId="f71ece23-5549-48d6-8af0-83d0f54e7adc"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Locked AzureResource DeleteError

<!--issueDescription-->

We have checked the cluster and it seems that cluster deletion failure is due to below resources were locked. 
***{ResourceName}*** 


<!--/issueDescription-->

To resolve the issue:
1. Please remove corresponding locks in your resource group 
2. If done, you can try it later

## **Recommended Documents**

* [Resource locks](https://docs.microsoft.com/en-us/azure/hdinsight/hadoop/hdinsight-troubleshoot-cluster-creation-fails#resources-locks)