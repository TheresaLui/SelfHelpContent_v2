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

If module errors occur, check the [module reference](https://docs.microsoft.com/azure/machine-learning/studio-module-reference/), or the [module error code](https://docs.microsoft.com/azure/machine-learning/studio-module-reference/errors/machine-learning-module-error-codes)

Following are some common errors and solutions:

- For errors such as "The input is not a valid Base-64 string as it contains a non-base 64 character, more than two padding characters, or an illegal character among the padding characters," make sure there are no white spaces in your input value.
- Errors may occur when you use **Import Data module** to import data from existing data storage that enables **Secure transfer required**. Since Studio (classic) only supports **HTTP**, check the configuration of your storage account in Azure portal and make sure that the **Secure transfer required** is disabled.

### Compute limitation

Studio (classic) has compute memory sku limitations. The compute is a shared host pool where one customer can use 8 cores, 56 GB at most for training. Memory can could also be affected by different machine learning algorithms and parameter settings. For a more powerful compute resource, consider using [Azure Machine Learning designer](https://docs.microsoft.com/azure/machine-learning/concept-designer).

## **Recommended Documents**

Microsoft Azure Machine Learning Studio (classic) is a collaborative, drag-and-drop tool you can use to build, test, and deploy predictive analytics solutions on your data. If you're currently using or evaluating Machine Learning Studio (classic), try [Azure Machine Learning designer](https://docs.microsoft.com/azure/machine-learning/concept-designer), which provides drag-and-drop ML modules, as well as scalability, version control, and enterprise security.
