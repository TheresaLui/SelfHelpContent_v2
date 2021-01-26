<properties
	pageTitle="Notebook not running"
	description="Notebook not running"
	infoBubbleText="Notebook not running"
	service="microsoft.machinelearning"
	resource="machinelearning"
	authors="abeomor"
	ms.author="osomorog"
	supportTopicIds="32739650"
	productPesIds="16644"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	articleId="microsoft.machinelearning.notebooks-notebooknotrunning"
	selfHelpType="generic"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Notebook not running

If your Notebook is not running, you might not be connected to a running compute instance. Most users are able to resolve Notebook issues by using the following steps.

## **Recommended Steps**
1. Check the Compute drop-down list and make sure your Notebook is connected to a running compute
2. If you are connected to a running Compute, skip to step 4. If not, click the **+** button in the toolbar and create a new Compute Instance. Or pick a running Compute Instance from the Compute drop-down list.
3. For a new Compute Instance, wait a few minutes for your Compute to start and then run a cell.
4. Your Compute Instance might have connection/authentication issues.
5. Click **Compute** in the Azure ML Studio menu bar
6. On the compute page, locate the Compute Instance with the issues
7. Try to restart the Compute Instance from that page
8. If the Notebook still doesn't run, make sure the Compute Instance is stopped and create a new one
9. Wait for the Compute Instance to reboot
10. Click **Notebooks** in the Azure ML Studio menu bar
11. Choose the same Compute Instance, and you should then be able to run a cell in a Notebook
12. If you're still having issues,  make sure your network is allowing websocket connections to `*.instances.azureml.net` and `*.instances.azureml.ms`

## **Recommended Documents**

* [How to run Jupyter Notebooks in your workspace](https://docs.microsoft.com/azure/machine-learning/how-to-run-jupyter-notebooks)
* [Clone Git repositories into your workspace file system](https://docs.microsoft.com/azure/machine-learning/concept-train-model-git-integration#clone-git-repositories-into-your-workspace-file-system)
* [What is an Azure Machine Learning compute instance?](https://docs.microsoft.com/azure/machine-learning/concept-compute-instance)
