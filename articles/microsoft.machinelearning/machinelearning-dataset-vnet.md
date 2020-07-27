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
	articleid="machinelearning-dataset-accessing-issues"
	ownershipId="AzureML_AzureMachineLearningServices"
/>


 
# Problem accessing dataset or connecting to datastore

 If you have problem accessing dataset or connecting to datastore, please find possible causes and steps to be taken as below:

## **Recommended Steps**

We recommend that you read the error message to understand the root cause and resolution. For your reference, here are a few things to verify when you run into errors while accessing your data: 
1. Network issues: Please verify if you are facing issues with your network

2. VNet issues: Check if your data is behind a Vnet or firewall. If so, you must use a workspace [managed identity](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fazure%2Factive-directory%2Fmanaged-identities-azure-resources%2Foverview&data=02%7C01%7Cxunwan%40microsoft.com%7C8d9cd159bcad4725008408d8300773b4%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637312155861208871&sdata=lmCOPbuvh%2F%2B3uZDfHjqqbEmdE6n%2BxBC8liyUxD0F27c%3D&reserved=0) to grant the Azure ML studio access to your data. Learn how to set up your environment to [access data behind virtual network](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fazure%2Fmachine-learning%2Fhow-to-enable-virtual-network&data=02%7C01%7Cxunwan%40microsoft.com%7C8d9cd159bcad4725008408d8300773b4%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637312155861208871&sdata=qoRMXKUukJEaA1mmakoUu%2BMGY6adS4lB8KwSMUOREeQ%3D&reserved=0)

3. Incorrect credentials: Verify if the credentials provided (SAS token or account key) for the datastore is correct and still active. If you are using ADLS Gen2, check out their access control set up to learn more: [access control set up for ADLS Gen 2](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fazure%2Fstorage%2Fblobs%2Fdata-lake-storage-access-control&data=02%7C01%7Cxunwan%40microsoft.com%7C8d9cd159bcad4725008408d8300773b4%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637312155861218870&sdata=dpqHkXbuCYwIjFs8zqAbGpjMIJUHr4fNI9ABLDJEN5g%3D&reserved=0)

4. Data deletion: Verify if the data you are trying to access was deleted from the storage account


## **Recommended Documents**

* [Connect to Azure storage services](https://docs.microsoft.com/azure/machine-learning/how-to-access-data)
* [Create Azure Machine Learning datasets](https://docs.microsoft.com/azure/machine-learning/how-to-create-register-datasets)
