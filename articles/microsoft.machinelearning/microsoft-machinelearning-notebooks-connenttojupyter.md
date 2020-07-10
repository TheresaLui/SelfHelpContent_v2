<properties
	pageTitle="Can't connect to Jupyter from my Notebook"
	description="Can't connect to Jupyter from my Notebook"
	infoBubbleText="Can't connect to Jupyter from my Notebook"
	service="microsoft.machinelearning"
	resource="machinelearning"
	authors="abeomor"
	ms.author="osomorog"
	supportTopicIds="32739645"
	productPesIds="16644"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	articleId="microsoft.machinelearning.notebooks-connecttojupyter"
	selfHelpType="generic"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Can't connect to Jupyter from my Notebook

If you can't connect to the terminal, your compute instance may have connection/authentication issues. Most users are able to resolve their Compute Instance issue by using the following steps.

## **Recommended Steps**
1. Click "Compute" in the Azure ML Studio menu bar
2. On the compute page locate the Compute Instance with the issues
3. Try to restart the Compute Instance from here
4. If the Jupyter continues to fail, make sure the Compute Instance is stopped and create a new one
5. Wait for the Compute Instance to reboot
6. Click "Notebooks" in the Azure ML Studio menu bar
7. Choose the same Compute Instance, and now you should be able to connect to the terminal

## **Recommended Documents**

If you are experiencing issues with Studio Notebooks, here is a list of resources which may be helpful:
* [How to run Jupyter Notebooks in your workspace](https://docs.microsoft.com/azure/machine-learning/how-to-run-jupyter-notebooks)
* [Clone Git repositories into your workspace file system](https://docs.microsoft.com/azure/machine-learning/concept-train-model-git-integration#clone-git-repositories-into-your-workspace-file-system)
* [What is an Azure Machine Learning compute instance?](https://docs.microsoft.com/azure/machine-learning/concept-compute-instance)
