<properties
	pageTitle="Problem creating or managing designer pipeline"
	description="Problem creating or managing designer pipeline"
	infoBubbleText="Problem creating or managing designer pipeline"
	service="microsoft.machinelearning"
	resource="designer"
	authors="likebupt"
	ms.author="keli19"
	articleId="machinelearning-designer-problemcreatingormanagingdesignerpipeline"
	selfHelpType="generic"
	supportTopicIds="32690871"
	productPesIds="16644"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Problem creating or managing designer pipeline

## **Recommended Steps**

1. If you cannot access Designer, it may be due to an RBAC issue. Ask your admin to check your permission.
1. If you are not clear about the module usage, see the [module reference documentation](https://docs.microsoft.com/azure/machine-learning/algorithm-module-reference/module-reference)
1. Also note the type of module port when you connect modules in the pipeline. DataFrameDirectory only supports tabular datasets.
1. If you cannot visualize the dataset or the module output, it might be due to some of the following reasons:
    - You can only visualize tabular dataset that's currently in Designer. Other file types do not support visualization.
    - Your dataset or module output is stored in the virtual network. You need to enable a workspace managed identity of the datastore in the **Update Credentials** setting panel.
    [Learn more](https://docs.microsoft.com/azure/machine-learning/resource-known-issues#dataset-visualization-in-the-designer).
1. You can also file an issue by clicking the smile icon in the top right corner of Azure Machine Learning studio with **including screenshot** selected, and with **Microsoft can email you about your feedback** selected in case we need to contact you regarding your specific case. Our engineering team will investigate.

## **Recommended Documents**

* [Manage access to an Azure Machine Learning workspace](https://docs.microsoft.com/azure/machine-learning/how-to-assign-roles)
* [Retrain models using pipeline parameter in the designer](https://docs.microsoft.com/azure/machine-learning/how-to-retrain-designer)
* [Run batch predictions using pipeline parameter in the designer](https://docs.microsoft.com/azure/machine-learning/how-to-run-batch-predictions-designer)
