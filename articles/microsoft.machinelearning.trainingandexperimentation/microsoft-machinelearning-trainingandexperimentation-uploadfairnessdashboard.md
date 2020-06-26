<properties
	pageTitle="Issues with uploading a fairness dashboard"
	description="Issues with uploading a fairness dashboard"
	infoBubbleText="Issues with uploading a fairness dashboard"
	service="microsoft.machinelearning"
	resource="trainingandexperimentation"
	authors="riedgar"
	ms.author="riedgar"
	supportTopicIds="????????"
	productPesIds="16644"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	articleId="microsoft.machinelearning.trainingandexperimentation.uploadfairnessdashboard"
	selfHelpType="generic"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Issues with uploading a fairness dashboard

## **Recommended Steps**
### Uploading a fairness dashboard from the SDK

Uploading a fairness dashboard for a model is a multi-step process:
1. Register the model (optional, but required by default)
1. Generate predictions from the model
1. Use Fairlearn to create the dictionary representation of the dashboard
1. Upload the dictionary representation using [`upload_dashboard_dictionary`](https://docs.microsoft.com/en-us/python/api/azureml-contrib-fairness/azureml.contrib.fairness?view=azure-ml-py#upload-dashboard-dictionary-run--dashboard-dict--dashboard-name--dataset-name-none--dataset-id-none--upload-bytes-limit-20971520--validate-model-ids-true-)

These stages are [shown in the sample notebooks](https://github.com/Azure/MachineLearningNotebooks/tree/master/contrib/fairness).

## **Recommended Documents**

For more information about fairness in machine learning [see the concept page](https://docs.microsoft.com/en-us/azure/machine-learning/concept-fairness-ml).
