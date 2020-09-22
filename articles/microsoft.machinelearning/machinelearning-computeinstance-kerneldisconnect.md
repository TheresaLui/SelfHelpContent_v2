<properties
  pagetitle="Problem Connecting to Jupyter, JupyterLab or RStudio"
  service="microsoft.machinelearningservices"
  resource="workspaces"
  ms.author="smishah"
  selfhelptype="Generic"
  supporttopicids="32745197"
  resourcetags="notebook,computeinstance"
  productpesids="16644"
  cloudenvironments="public,fairfax,mooncake,usnat,ussec"
  articleid="microsoft.machinelearning.computeinstance.kerneldisconnect"
  ownershipid="AzureML_AzureMachineLearningServices" />
# Problem Connecting to Jupyter, JupyterLab or RStudio

This section helps with issues connecting to Compute instance through Jupyter, JupyterLab and RStudio and running your notebooks.

## **Recommended Steps**

- If compute instance is created behind VNET, make sure you have NSG rule where compute instance inbound TCP traffic on port 44224 is allowed from a Service Tag of AzureMachineLearning
- If you are behind a proxy ensure that web socket communication is not disabled for azureml.net and azureml.ms domains
- Try restarting the Compute Instance and then rerunning the notebook