<properties
	pageTitle="Custom DNS or NSG UDR setting issue"
	description="Custom DNS or NSG UDR setting issue"
	service=""
	resource=""
	authors="rimayber"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="fb2787b0-c8e5-4137-9211-dd2986938301"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Custom DNS or NSG UDR setting issue

<!--issueDescription-->

We have checked the cluster and it seems that cluster creation failure is due to an issue with the custom DNS setup or NSG and UDR setting<br>
<br>
To resolve the issue:<br>
<br>
1. Please follow the recommended document 1 to check custom DNS setup<br>
2. Please follow the recommended document 2 to check NSG and UDR<br>

<!--/issueDescription-->

## Recommended documents

1. [Virtual network is not compatible](https://docs.microsoft.com/en-us/azure/hdinsight/hadoop/troubleshoot-invalidnetworkconfigurationerrorcode-cluster-creation-fails#virtual-network-configuration-is-not-compatible-with-hdinsight-requirement)
2. [Failed to connect to Azure Storage](https://docs.microsoft.com/en-us/azure/hdinsight/hadoop/troubleshoot-invalidnetworkconfigurationerrorcode-cluster-creation-fails#failed-to-connect-to-azure-storage-account)