<properties
	pageTitle="Can’t access Notebook shared with me by URL"
	description="Can’t access Notebook shared with me by URL"
	infoBubbleText="Can’t access Notebook shared with me by URL"
	service="microsoft.machinelearning"
	resource="machinelearning"
	authors="abeomor"
	ms.author="osomorog"
	supportTopicIds="32739643"
	productPesIds="16644"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	articleId="microsoft.machinelearning.notebooks-accesssharednotebook"
	selfHelpType="generic"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Can’t access Notebook shared with me by URL

To view shared Notebooks you have to have access to the workspace. Most users are able to resolve their Notebook access issue by asking the user that sent the link to complete the following steps.

## **Recommended Steps**

Make sure the user you sent the link to has access to your workspace:

1. In the Azure Portal, search "Machine Learning" 
2. Click the "Machine Learning" service 
3. Find your workspace, and click your workspace name to open the Machine Learning Workspace blade
4. Go to "Access Control (IAM)"
3. Check if the user you send the link to has access to your workspace
4. If the user doesn't have access, click the "+ Add" button
5. Add the user and assign the appropriate level of access

Note: Reader access is the minimum level of access to view a shared Notebook.

## **Recommended Documents**

If you are experiencing issues with Studio Notebooks, here is a list of resources which may be helpful:

* [How to run Jupyter Notebooks in your workspace](https://docs.microsoft.com/azure/machine-learning/how-to-run-jupyter-notebooks)
* [Clone Git repositories into your workspace file system](https://docs.microsoft.com/azure/machine-learning/concept-train-model-git-integration#clone-git-repositories-into-your-workspace-file-system)
* [What is an Azure Machine Learning compute instance?](https://docs.microsoft.com/azure/machine-learning/concept-compute-instance)
