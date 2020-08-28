<properties
	pageTitle="Stuck or failed experiment"
	description="Stuck or failed experiment"
	infoBubbleText="Stuck or failed experiment"
	service="microsoft.machinelearningstudioclassic"
	resource="studioclassic"
	authors="likebupt"
	ms.author="keli19"
	articleId="machinelearning-studioclassic-stuckorfailedexperiment"
	selfHelpType="generic"
	supportTopicIds="32355159"
	productPesIds="15570"
	cloudEnvironments="public, usnat, ussec"
	ownershipId="AzureML_StudioClassicServices"
/>

# Stuck or failed experiment

## **Recommended Steps**

Studio (classic) has compute memory sku limitation. Actually the compute is a shared host pool where one customer can use 8 cores, 56GB at most for training. Memory cost could also be affected by different machine learning algorithms and parameter settings. For more powerful compute resource, please consider using [Azure Machine Learning designer](https://docs.microsoft.com/azure/machine-learning/concept-designer).

## **Recommended Documents**
Microsoft Azure Machine Learning Studio (classic) is a collaborative, drag-and-drop tool you can use to build, test, and deploy predictive analytics solutions on your data. Customers currently using or evaluating Machine Learning Studio (classic) are encouraged to try [Azure Machine Learning designer](https://docs.microsoft.com/azure/machine-learning/concept-designer), which provides drag and drop ML modules plus scalability, version control, and enterprise security.