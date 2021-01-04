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

Most users can resolve issues with running notebooks on compute instance by using the following steps.

## **Recommended Steps**

- See the [list of tools and packages installed on compute instance](https://docs.microsoft.com/azure/machine-learning/concept-compute-instance#contents)
- Only the creator of compute instance is able to run notebooks on the compute instance. However, there is a "create on behalf of" feature in preview that allows administrators to create and assign a compute instance to another user to run notebooks.
- If compute instance is created behind VNet, make sure you have an NSG rule where compute instance inbound TCP traffic on port 44224 is allowed from a Service Tag of AzureMachineLearning. If you are behind a proxy, make sure that web socket communication is not disabled for azureml.net and azureml.ms domains. If workspace storage account is attached to a virtual network please ensure compute instance is also deployed to same virtual network/subnet. If you are using custom DNS please check you settings. See [documentation for virtual network setup](https://docs.microsoft.com/azure/machine-learning/how-to-secure-training-vnet#compute-instance).
- If you've created a compute instance in a private link workspace, ensure that you're accessing the compute instance from within virtual network. If you're using custom DNS or a host file, ensure that you have an entry for `<instance-name>.<region>.instances.azureml.ms` with a private IP address of the workspace private endpoint. If you are using custom DNS you might need to setup a DNS forwarder. You also need to setup a private endpoint to Azure file share if workspace storage is using private link.[Learn more](https://docs.microsoft.com/azure/machine-learning/how-to-custom-dns?tabs=azure-portal).
- Configure firewall and user-defined routes according to [these instructions](https://docs.microsoft.com/azure/machine-learning/how-to-access-azureml-behind-firewall)
- Try restarting the compute instance and then re-running the notebook
- If the notebook is running slowly, check the CPU/GPU usage on the compute instance
- If you are trying to download files on the compute instance, use a single TCP session to download all the files
- For package management within a notebook, use `%pip` or `%conda` magic functions to automatically install packages into the currently-running kernel, rather than `!pip` or `!conda`
- If you are trying to pip install `pytesseract`, you need to perform "sudo apt install tesseract-ocr"
- Do not delete the `azureml_py36` conda environment or Python 3.6 - AzureML kernel. These are needed for Jupyter/JupyterLab functionality.
- If you need to download temporary data to a compute instance, use the temporary disk (/mnt)
- Currently, we don't support auto-shutdown on a compute instance
- For creating a compute instance the following RBAC permissions are needed : *Microsoft.MachineLearningServices/workspaces/computes/write* *Microsoft.MachineLearningServices/workspaces/checkComputeNameAvailability/action*

