<properties
	pageTitle="File not showing up"
	description="File not showing up"
	infoBubbleText="File not showing up"
	service="microsoft.machinelearning"
	resource="machinelearning"
	authors="abeomor"
	ms.author="osomorog"
	supportTopicIds="32739649"
	productPesIds="16644"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	articleId="microsoft.machinelearning.notebooks-filesnotshowing"
	selfHelpType="generic"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# File not showing up

If your file is not showing up in the File Explorer, your might have saved the file outside of the Users directory. Most users are able to resolve their File Explorer issue by using the following steps.

## **Recommended Steps**

1. Make sure your files and folders anywhere under the **~/cloudfiles/code/Users** folder so they will be visible in all your Jupyter environments
2. If your workspace is in a **sovereign cloud**, such as Azure Government or Azure China 21Vianet, notebooks do not support using storage that is in a virtual network. Instead, you can use Jupyter Notebooks from a compute instance. For more information, about [working in a VNET](https://docs.microsoft.com/azure/machine-learning/how-to-enable-studio-virtual-network).

## **Recommended Documents**

If you are experiencing issues with Studio Notebooks, here is a list of resources which may be helpful:

* [How to run Jupyter Notebooks in your workspace](https://docs.microsoft.com/azure/machine-learning/how-to-run-jupyter-notebooks)
* [Clone Git repositories into your workspace file system](https://docs.microsoft.com/azure/machine-learning/concept-train-model-git-integration#clone-git-repositories-into-your-workspace-file-system)
* [What is an Azure Machine Learning compute instance?](https://docs.microsoft.com/azure/machine-learning/concept-compute-instance)
