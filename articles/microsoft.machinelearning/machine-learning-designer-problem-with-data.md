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

Use the following steps to troubleshoot datasets issues in the Azure Machine Learning designer.

## **Recommended Steps**

* **Cannot visualize output data of a module**

    This might be caused by:
    1. An unsupported dataset type. Currently, designer only supports visualization of tabular dataset. If you register your dataset as a file dataset type outside the designer, it can't be visualized when you drag it to build pipeline within the designer.
    2. Your storage is behind VNet. Make sure to follow [this article](https://docs.microsoft.com/azure/machine-learning/how-to-enable-studio-virtual-network) to enable using AML studio in an Azure virtual network.

* **`NaN` values in datasets**

    If a column of your dataset has a `NaN` value, you must specify the data type of this column as **decimal** when registering the dataset to workspace. This corresponds to float64 in pandas DataFrame. If you specify it as **integer**, the value will be marked as "Error" at the time of registration and cannot be correctly processed by designer modules.


## **Recommended Documents**

* [What is Azure Machine Learning designer?](https://docs.microsoft.com/azure/machine-learning/concept-designer)
* [Import data to designer](https://docs.microsoft.com/azure/machine-learning/how-to-designer-import-data)
* [Retrain models using pipeline parameter in the designer](https://docs.microsoft.com/azure/machine-learning/how-to-retrain-designer)
* [Run batch predictions using pipeline parameter in the designer](https://docs.microsoft.com/azure/machine-learning/how-to-run-batch-predictions-designer)
