<properties
	pageTitle="Problems with fairness dashboards"
	description="Problems with fairness dashboards"
	infoBubbleText="Problems with fairness dashboards"
	service="microsoft.machinelearning"
	resource="trainingandexperimentation"
	authors="riedgar"
	ms.author="riedgar"
	supportTopicIds="32745199"
	productPesIds="16644"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	articleId="microsoft.machinelearning.trainingandexperimentation.problemsfairnessdashboard"
	selfHelpType="generic"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Problems with fairness dashboards

## **Recommended Steps**
### Uploading a fairness dashboard from the SDK

Uploading a fairness dashboard for a model is a multi-step process:
1. Register the model (optional, but required by default)
1. Generate predictions from the model
1. Use Fairlearn to create the dictionary representation of the dashboard
1. Upload the dictionary representation using [`upload_dashboard_dictionary`](https://docs.microsoft.com/python/api/azureml-contrib-fairness/azureml.contrib.fairness?view=azure-ml-py#upload-dashboard-dictionary-run--dashboard-dict--dashboard-name--dataset-name-none--dataset-id-none--upload-bytes-limit-20971520--validate-model-ids-true-)

These stages are [shown in the sample notebooks](https://github.com/Azure/MachineLearningNotebooks/tree/master/contrib/fairness).


### Accessing the fairness dashboard from the UI
If a Run uploaded fairness statistics, then they will appear as a tab on the run's history. To access the run history from the Azure Machine Learning studio client, navigate to the "Experiment" tab view and click on the corresponding experiment. Each of the runs in that experiment are then accessible from the list view. Click on the appropriate run to access its history page, and the fairness dashboard will be available on the 'Fairness' tab.


## **Recommended Documents**

For more information about fairness in machine learning [see the concept page](https://docs.microsoft.com/azure/machine-learning/concept-fairness-ml).
