<properties
	pageTitle="Problem with web service plan (Commitment plan)"
	description="Problem with web service plan (Commitment plan)"
	infoBubbleText="Problem with web service plan (Commitment plan)"
	service="microsoft.machinelearningstudioclassic"
	resource="studioclassic"
	authors="likebupt"
	ms.author="keli19"
	articleId="machinelearning-studioclassic-problemwithwebserviceplancommitmentplan"
	selfHelpType="generic"
	supportTopicIds="32321847"
	productPesIds="15570"
	cloudEnvironments="public, usnat, ussec, fairfax"
	ownershipId="AzureML_AzureMachineLearning"
/>

# Problem with web service plan (Commitment plan)

## **Recommended Steps**

1. Workspace deletion independent from commitment plan. User need to delete them respectively in [Azure portal](https://ms.portal.azure.com/#home) and [web services portal](https://services.azureml.net/plans/).
1. After a workspace is deleted, web services in this workspace ought to be unavailable and cleaned up by design. There may be rare cases in which web services cannot be deleted successfully when deleting a workspace.

## **Recommended Documents**

Microsoft Azure Machine Learning Studio (classic) is a collaborative, drag-and-drop tool you can use to build, test, and deploy predictive analytics solutions on your data. Customers currently using or evaluating Machine Learning Studio (classic) are encouraged to try [Azure Machine Learning designer](https://docs.microsoft.com/azure/machine-learning/concept-designer), which provides drag and drop ML modules plus scalability, version control, and enterprise security.
