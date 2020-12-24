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
- If compute instance is created behind VNET, make sure you have an NSG rule where compute instance inbound TCP traffic on port 44224 is allowed from a Service Tag of AzureMachineLearning. If you are behind a proxy ensure where web socket communication is not disabled for azureml.net and azureml.ms domains, see [documentation for virtual network setup](https://docs.microsoft.com/azure/machine-learning/how-to-secure-training-vnet#compute-instance).
- If you've created compute instance in a private link workspace, ensure that you're accessing the compute instance from within virtual network. If you're using custom DNS or a host file, ensure that you have an entry for `<instance-name>.<region>.instances.azureml.ms` with a private IP address of the workspace private endpoint. [Learn more](https://docs.microsoft.com/azure/machine-learning/how-to-custom-dns?tabs=azure-portal)
- Configure firewall and user defined routes according to this document (https://docs.microsoft.com/azure/machine-learning/how-to-access-azureml-behind-firewall)
- Try restarting the compute instance and then re-running the notebook
- If the notebook is running slowly, check the CPU/GPU usage on the compute instance
- If you are trying to download files on the compute instance, use a single TCP session to download all the files
- For package management within a notebook, use %pip or %conda magic functions to automatically install packages into the currently-running kernel, rather than !pip or !conda
- If you are trying to pip install pytesseract then you need to do "sudo apt install tesseract-ocr"
- Please do not delete the azureml_py36 conda environment or Python 3.6 - AzureML kernel. This is needed for Jupyter/JupyterLab functionality
- If you need to download temp data on to compute instance please use the temp disk (/mnt)
- At this time we don't support auto-shutdown on compute instance

