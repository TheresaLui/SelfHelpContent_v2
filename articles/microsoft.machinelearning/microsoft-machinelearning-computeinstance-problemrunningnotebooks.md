<properties 
    pageTitle="Problem running notebooks on compute instance"
    description="Problem running notebooks on compute instance"
    service="microsoft.machinelearning"
    resource="computeinstance"
    authors="hustcrystal"
    ms.author="vijetajo"
    displayOrder="1"
    selfHelpType="resource"
    supportTopicIds="32745198"
    resourceTags="notebook,computeinstance"
    productPesIds="16644"
    cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
    articleId="microsoft.machinelearning.computeinstance.problemrunningnotebooks"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Problem running notebooks on compute instance

This section helps with issues running your notebooks on compute instance

## **Recommended Steps**

- Please find here the list of tools and packages installed on compute instance https://docs.microsoft.com/azure/machine-learning/concept-compute-instance#contents
- Only the creator of compute instance is able to run notebooks on the compute instance. However, there is create on behalf of feature in preview which allows admin to create and assign a compute instance to another user to run notebooks.
- If compute instance is created behind VNET, make sure you have NSG rule where compute instance inbound TCP traffic on port 44224 is allowed from a Service Tag of AzureMachineLearning
- If you are behind a proxy ensure that web socket communication is not disabled for azureml.net and azureml.ms domains
- Try restarting the Compute Instance and then rerunning the notebook
- If the notebook is running slowly check the CPU/GPU usage on compute instance
- If you are trying to download files on compute instance please use a single TCP session to download all the files
