<properties
	pageTitle="Can't connect to Jupyter or VSCode from my Notebook"
	description="Can't connect to Jupyter or VSCode from my Notebook"
	infoBubbleText="Can't connect to Jupyter or VSCode from my Notebook"
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

# Can't connect to Jupyter or VSCode from my Notebook

If you can't connect to the VSCode or Jupyter Notebook, your compute instance may have connection or authentication issues. Most users are able to resolve their compute instance issue by using the following steps.

## **Recommended Steps**
1. Select **Compute** in the Azure ML Studio menu
2. On the **Compute** page, locate the compute instance with the issues, and restart it
3. If Jupyter continues to fail, make sure the compute instance is stopped, and create a new one
4. Wait for the compute instance to reboot
5. In the Azure ML Studio menu, select **Notebooks** 
6. Select the same compute instance. You should now be able to open a Notebook, select **Editors** in the **Notebook** menu and connect to Jupyter/VSCode.


## Considerations

* If the compute instance is created behind a VNet, make sure that you have a Network Security Group (NSG) rule where compute instance inbound TCP traffic on port 44224 is allowed from a Service Tag of AzureMachineLearning.
* If you're behind a proxy, ensure that your network allows websocket connections to `.instances.azureml.net` and `.instances.azureml.ms`.

## **Recommended Documents**

If you are experiencing issues with Studio Notebooks, here is a list of resources which may be helpful:
* [Virtual network setup in Azure ML](https://docs.microsoft.com/azure/machine-learning/how-to-secure-training-vnet?WT.mc_id=Portal-Microsoft_Azure_Support#compute-instance)
* [How to run Jupyter Notebooks in your workspace](https://docs.microsoft.com/azure/machine-learning/how-to-run-jupyter-notebooks)
* [Clone Git repositories into your workspace file system](https://docs.microsoft.com/azure/machine-learning/concept-train-model-git-integration#clone-git-repositories-into-your-workspace-file-system)
* [What is an Azure Machine Learning compute instance?](https://docs.microsoft.com/azure/machine-learning/concept-compute-instance)
