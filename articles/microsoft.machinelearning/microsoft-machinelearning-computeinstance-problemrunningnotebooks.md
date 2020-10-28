<properties
  pagetitle="Problem running notebooks on compute instance"
  service="microsoft.machinelearning"
  resource="computeinstance"
  ms.author="vijetajo,smishah"
  selfhelptype="Generic"
  supporttopicids="32745198"
  resourcetags="notebook,computeinstance"
  productpesids="16644"
  cloudenvironments="public,fairfax,mooncake,usnat,ussec"
  articleid="microsoft.machinelearning.computeinstance.problemrunningnotebooks"
  ownershipid="AzureML_AzureMachineLearningServices" />
# Problem running notebooks on compute instance

This section helps with issues running your notebooks on compute instance

## **Recommended Steps**

- Please find here the [list of tools and packages installed on compute instance](https://docs.microsoft.com/azure/machine-learning/concept-compute-instance#contents)
- Only the creator of compute instance is able to run notebooks on the compute instance. However, there is create on behalf of feature in preview which allows admin to create and assign a compute instance to another user to run notebooks.
- If compute instance is created behind VNET, make sure you have NSG rule where compute instance inbound TCP traffic on port 44224 is allowed from a Service Tag of AzureMachineLearning. If you are behind a proxy ensure that web socket communication is not disabled for azureml.net and azureml.ms domains. Please refer to documentation here for virtual network setup https://docs.microsoft.com/en-us/azure/machine-learning/how-to-secure-training-vnet#compute-instance
- If you have created compute instance in a private link workspace please ensure that you are accessing the compute instance from within virtual network. If you are using custom DNS or host file please ensure you have an entry for <instance-name>.<region>.instances.azureml.ms with private IP address of workspace private endpoint. For more details please look at documentation here https://docs.microsoft.com/en-us/azure/machine-learning/how-to-custom-dns?tabs=azure-portal
- Try restarting the Compute Instance and then rerunning the notebook
- If the notebook is running slowly check the CPU/GPU usage on compute instance
- If you are trying to download files on compute instance please use a single TCP session to download all the files
