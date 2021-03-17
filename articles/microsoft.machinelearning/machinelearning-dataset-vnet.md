<properties
  pagetitle="Problem accessing dataset or connecting to datastore"
  service="microsoft.machinelearning"
  resource="datasets"
  ms.author="xunwan"
  selfhelptype="Generic"
  supporttopicids="32690860"
  resourcetags=""
  productpesids="16644"
  cloudenvironments="public,fairfax,mooncake,usnat,ussec"
  articleid="machinelearning-dataset-vnet"
  ownershipid="AzureML_AzureMachineLearningServices" />
# Problem accessing dataset or connecting to datastore

 If you have problem accessing dataset or connecting to datastore, please find possible causes and steps to be taken as below:

## **Recommended Steps**

We recommend that you read the error message to understand the root cause and resolution. For your reference, here are a few things to verify when you run into errors while accessing your data: 

1. **Network issues**: Please verify if you are facing issues with your network
2. **VNet issues**: Check if your data storage is behind a Vnet or firewall. If so, you must make sure your [Storage's Vnet setting is correct](https://docs.microsoft.com/azure/machine-learning/how-to-secure-workspace-vnet#secure-azure-storage-accounts).
3. **Incorrect credentials**: Verify if the credentials provided (SAS token or account key) for the datastore is correct and still active. If you are using ADLS Gen2, check out their access control set up to learn more: [access control set up for ADLS Gen 2](https://docs.microsoft.com/azure/storage/blobs/data-lake-storage-access-control).
4. **Data deletion**: Verify if the data you are trying to access was deleted from the storage account
5. **FileNotExist error**: If you get similar error message as "cannot open file '/xxx/yyy/zzz.tsv': No such file or directory", please make sure the directory you are using exists

## **Recommended Documents**

* [Connect to Azure storage services](https://docs.microsoft.com/azure/machine-learning/how-to-access-data)
* [Create Azure Machine Learning datasets](https://docs.microsoft.com/azure/machine-learning/how-to-create-register-datasets)
* [Use dataset in pipeline](https://github.com/Azure/MachineLearningNotebooks/tree/master/how-to-use-azureml/work-with-data/datasets-tutorial/pipeline-with-datasets)
* [Use dataset in scriptrun](https://github.com/Azure/MachineLearningNotebooks/tree/master/how-to-use-azureml/work-with-data/datasets-tutorial/scriptrun-with-data-input-output)
