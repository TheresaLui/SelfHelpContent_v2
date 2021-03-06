<properties
  pagetitle="Problem Connecting to VSCode, Jupyter, JupyterLab or RStudio"
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
# Problem Connecting to VSCode, Jupyter, JupyterLab or RStudio

This section helps with issues connecting to compute instance through VSCode, Jupyter, JupyterLab, RStudio, and running your notebooks.

## **Recommended Steps**

- If the compute instance is created behind a VNet, make sure that you have an NSG rule where compute instance inbound TCP traffic on port 44224 is allowed from a Service Tag of AzureMachineLearning. 
- If you're behind a proxy, ensure that web socket communication is not disabled for the `azureml.net` and `azureml.ms` domains. 
- Try restarting the compute instance and rerunning the notebook. 
- For details, see [documentation for virtual network setup](https://docs.microsoft.com/azure/machine-learning/how-to-secure-training-vnet#compute-instance)
