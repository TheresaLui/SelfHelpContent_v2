<properties
	pageTitle="Problem creating or running existing experiment"
	description="Problem creating or running existing experiment"
	infoBubbleText="Problem creating or running existing experiment"
	service="microsoft.machinelearningstudioclassic"
	resource="studioclassic"
	authors="likebupt"
	ms.author="keli19"
	articleId="machinelearning-studioclassic-problemcreatingorrunningexistingexperiment"
	selfHelpType="generic"
	supportTopicIds="32321848"
	productPesIds="15570"
	cloudEnvironments="public, usnat, ussec, fairfax"
	ownershipId="AzureML_AzureMachineLearning"
/>

# Problem creating or running existing experiment

## **Recommended Steps**

### Module error

If module errors occur, please check [module reference](https://docs.microsoft.com/azure/machine-learning/studio-module-reference/), or [module error code](https://docs.microsoft.com/azure/machine-learning/studio-module-reference/errors/machine-learning-module-error-codes)

Following are some common errors and solutions:

- Specifically for errors like "The input is not a valid Base-64 string as it contains a non-base 64 character, more than two padding characters, or an illegal character among the padding characters.", please make sure there are no white spaces in your input value.
- Error may occur when you use **Import Data module** to import data from existing data storage which enables **Secure transfer required**. Since Studio (classic) only supports **HTTP**, please check the configuration of your storage account in Azure portal, and make sure the **Secure transfer required** is disabled.

### Compute limitation

Studio (classic) has compute memory sku limitation. The compute is a shared host pool where one customer can use 8 cores, 56GB at most for training. Memory cost could also be affected by different machine learning algorithms and parameter settings. For more powerful compute resource, please consider using [Azure Machine Learning designer](https://docs.microsoft.com/azure/machine-learning/concept-designer).

## **Recommended Documents**

Microsoft Azure Machine Learning Studio (classic) is a collaborative, drag-and-drop tool you can use to build, test, and deploy predictive analytics solutions on your data. Customers currently using or evaluating Machine Learning Studio (classic) are encouraged to try [Azure Machine Learning designer](https://docs.microsoft.com/azure/machine-learning/concept-designer), which provides drag and drop ML modules plus scalability, version control, and enterprise security.
