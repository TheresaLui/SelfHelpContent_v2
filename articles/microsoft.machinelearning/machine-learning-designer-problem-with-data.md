<properties
	pageTitle="Problem of datasets in the designer"
	description="Problem of datasets in the designer"
	infoBubbleText="Problem of datasets in the designer"
	service="microsoft.machinelearning"
	resource="designer"
	authors="likebupt"
	ms.author="keli19"
	articleId="machine-learning-designer-problem-with-data"
	selfHelpType="generic"
	supportTopicIds="32789516"
	productPesIds="16644"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Problem of datasets in the designer

## **Recommended Steps**

* Cannot visualize output data of a module

    This might be due to one of the following reasons:
    1. Currently, designer only supports visualization of tabular dataset. If you register your dataset as file dataset type outside the designer, then when you drag it to build pipeline in the designer, it cannot be visualized.
    2. If your storage is behind Vnet, error may occur when you visualize the module output. Make sure that you have followed [this article](https://docs.microsoft.com/azure/machine-learning/how-to-enable-studio-virtual-network) to enable using AML studio in an Azure virtual network.

* "NaN" value in dataset

    If some column of your dataset has "NaN" value, when register dataset to workspace, the data type of this column must be specified in "decimal", which corresponds to float64 in pandas DataFrame. If you set it to "integer", the value will be marked as "Error" at the time of registration and cannot be correctly processed by Designer modules.


## **Recommended Documents**

* [What is Azure Machine Learning designer?](https://docs.microsoft.com/azure/machine-learning/concept-designer)
* [Import data to designer](https://docs.microsoft.com/azure/machine-learning/how-to-designer-import-data)
* [Retrain models using pipeline parameter in the designer](https://docs.microsoft.com/azure/machine-learning/how-to-retrain-designer)
* [Run batch predictions using pipeline parameter in the designer](https://docs.microsoft.com/azure/machine-learning/how-to-run-batch-predictions-designer)
