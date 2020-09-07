<properties
	pageTitle="Problem accessing dataset or connecting to datastore"
	description="Problem accessing dataset or connecting to datastore: possible causes and steps to be taken"
	service="microsoft.machinelearning"
	resource="datasets"
	authors="SturgeonMi"
	ms.author="xunwan"
	selfHelpType="generic"
	supportTopicIds="32690860"
	resourceTags=""
	productPesIds="16644"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	articleid="machinelearning-dataset-vnet"
	ownershipId="AzureML_AzureMachineLearningServices"
/>
# Problem accessing dataset or connecting to datastore

 If you have problem accessing dataset or connecting to datastore, please find possible causes and steps to be taken as below:

## **Recommended Steps**

We recommend that you read the error message to understand the root cause and resolution. For your reference, here are a few things to verify when you run into errors while accessing your data: 

1. **Network issues**: Please verify if you are facing issues with your network
2. **VNet issues**: Check if your data is behind a Vnet or firewall. If so, you must use a workspace [managed identity](https://docs.microsoft.com/azure/active-directory/managed-identities-azure-resources/overview) to grant the Azure ML studio access to your data. Learn how to set up your environment to [access data behind virtual network](https://docs.microsoft.com/azure/machine-learning/how-to-enable-virtual-network).
3. **Incorrect credentials**: Verify if the credentials provided (SAS token or account key) for the datastore is correct and still active. If you are using ADLS Gen2, check out their access control set up to learn more: [access control set up for ADLS Gen 2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-access-control).
4. **Data deletion**: Verify if the data you are trying to access was deleted from the storage account
5. **FIleNotExist error**: If you get similar error message as "cannot open file '/xxx/yyy/zzz.tsv': No such file or directory", please make sure the directory you are using exists

## **Recommended Documents**

* [Connect to Azure storage services](https://docs.microsoft.com/azure/machine-learning/how-to-access-data)
* [Create Azure Machine Learning datasets](https://docs.microsoft.com/azure/machine-learning/how-to-create-register-datasets)
