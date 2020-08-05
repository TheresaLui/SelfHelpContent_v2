<properties
	pageTitle="Deploying Automated ML Models"
	description="Deploying Automated ML Models"
	infoBubbleText="Deploying Automated ML Models"
	service="microsoft.machinelearning.automl"
	resource="automl"
	authors="Sabina"
	ms.author="sacartac"
	supportTopicIds="32690853"
	productPesIds="16644"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	articleId="microsoft.machinelearning.automl.deployment"
	selfHelpType="generic"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Deploying Automated ML Models

Here you will learn how to deploy your AutoML models.

### Using the SDK

The workflow is similar no matter where you deploy your model: 

1. [Retrieve the Best Model](https://docs.microsoft.com/azure/machine-learning/tutorial-auto-train-models#retrieve-the-best-model): Below we select the best pipeline from our iterations. The get_output method returns the best run and the fitted model. Overloads on get_output allow you to retrieve the best run and fitted model for any logged metric or for a particular iteration.

```
best_run, fitted_model = remote_run.get_output()

model_name = best_run.properties['model_name']
script_file_name = 'inference/score.py'
best_run.download_file('outputs/scoring_file_v_1_0_0.py', 'inference/score.py')
```

2. [Register the Fitted Model for Deployment](https://docs.microsoft.com/azure/machine-learning/how-to-deploy-and-where#registermodel): If neither metric nor iteration are specified in the register_model call, the iteration with the best primary metric is registered

```
description = 'AutoML Model trained on bank marketing data to predict if a client will subscribe to a term deposit'
tags = None
model = remote_run.register_model(model_name = model_name, description = description, tags = tags)

print(remote_run.model_id) # This will be written to the script file later in the notebook.
```

3. [Prepare](https://docs.microsoft.com/azure/machine-learning/how-to-deploy-and-where#prepare-to-deploy) to deploy. Specify assets, usage, compute target.

1. [Deploy to target](https://docs.microsoft.com/azure/machine-learning/how-to-deploy-and-where#deploy-to-target): Deployment uses the inference configuration deployment configuration to deploy the models. The deployment process is similar regardless of the compute target. Deploying to Azure Kubernetes Service (AKS) is slightly different because you must provide a reference to the AKS cluster. 

4. [Test](https://docs.microsoft.com/azure/machine-learning/how-to-consume-web-service) the deployed model, also called a web service

### Using the User Interface

Once you have the best model at hand, it is time to deploy it as a web service to predict on new data.

Automated ML helps you with deploying the model without writing code:

1. You have a couple options for deployment:

* Option 1: Deploy the best model, according to the metric criteria you defined:
	
	1. After the experiment is complete, navigate to the parent run page by selecting **Run 1** at the top of the screen
	1. Select the model listed in the **Best model summary** section
	1. Select **Deploy** on the top left of the window

* Option 2: To deploy a specific model iteration from this experiment:

	1. Select the desired model from the **Models** tab
	1. Select **Deploy** on the top left of the window

2. Populate the **Deploy model** pane:

Field| Value
----|----
Name| Enter a unique name for your deployment
Description| Enter a description to better identify what this deployment is for
Compute type| Select the type of endpoint you want to deploy: *Azure Kubernetes Service (AKS)* or *Azure Container Instance (ACI)*
Compute name| *Applies to AKS only:* Select the name of the AKS cluster you wish to deploy to
Enable authentication | Select to allow for token-based or key-based authentication

Use custom deployment assets| Enable this feature if you want to upload your own scoring script and environment file. [Learn more about scoring scripts](https://docs.microsoft.com/azure/machine-learning/how-to-deploy-and-where#script).

**NOTE**: File names must be under 32 characters and must begin and end with alphanumerics. May include dashes, underscores, dots, and alphanumerics between. Spaces are not allowed.

The *Advanced* menu offers default deployment features such as [data collection](https://docs.microsoft.com/azure/machine-learning/how-to-enable-app-insights) and resource utilization settings. If you wish to override these defaults do so in this menu.

3. Select **Deploy**. Deployment can take about 20 minutes to complete. Once deployment begins, the **Model summary** tab appears. See the deployment progress under the **Deploy status** section. 

Now you have an operational web service to generate predictions! You can test the predictions by querying the service from [Power BI's built in Azure Machine Learning support](https://docs.microsoft.com/azure/machine-learning/how-to-consume-web-service#consume-the-service-from-power-bi).

## **Recommended Documents**

* [Deploy models with Azure Machine Learning](https://docs.microsoft.com/azure/machine-learning/how-to-deploy-and-where)
* [Consume an Azure Machine Learning Model](https://docs.microsoft.com/azure/machine-learning/how-to-consume-web-service)
* [Deploy your model using the UI](https://docs.microsoft.com/azure/machine-learning/how-to-use-automated-ml-for-ml-models#deploy-your-model)
* [Known issues and troubleshooting in Azure Machine Learning](https://docs.microsoft.com/azure/machine-learning/resource-known-issues#automated-machine-learning)
* [Sample Notebook: deploying to ACI](https://github.com/Azure/MachineLearningNotebooks/blob/master/how-to-use-azureml/automated-machine-learning/classification-bank-marketing-all-features/auto-ml-classification-bank-marketing-all-features.ipynb)
* [Sample Notebook: deploying to AKS](https://github.com/Azure/MachineLearningNotebooks/tree/master/how-to-use-azureml/deployment/production-deploy-to-aks)
* [Sample Notebook: general deployment](https://github.com/Azure/MachineLearningNotebooks/tree/master/how-to-use-azureml/deployment)
