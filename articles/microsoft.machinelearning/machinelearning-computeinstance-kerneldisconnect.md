<properties 
    pageTitle="Problem Connecting to Jupyter, JupyterLab, RStudio"
    description="Problem Connecting to Jupyter, JupyterLab, RStudio"
    service="microsoft.machinelearning"
    resource="computeinstance"
    authors="hustcrystal"
    ms.author="chrjia, femi.olukoya"
    displayOrder="1"
    selfHelpType="resource"
    supportTopicIds="32745197"
    resourceTags="notebook,computeinstance"
    productPesIds="16644"
    cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
    articleId="microsoft.machinelearning.computeinstance.kerneldisconnect"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Problem Connecting to Jupyter, JupyterLab, RStudio

This section helps with issues connecting to Compute instance through Jupyter, JupyterLab and RStudio and running your notebooks.

## **Recommended Steps**
- If compute instance is created behind VNET make sure you have NSG rule where compute instance inbound TCP traffic on port 44224 is allowed from a Service Tag of AzureMachineLearning.
- If you are behind a proxy ensure that web socket communication is not disabled for azureml.net and azureml.ms domains
- Try restarting the Compute Instance and then rerunning the notebook
