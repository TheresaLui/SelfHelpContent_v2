<properties
	pageTitle="Running an Automated ML Experiment"
	description="Running an Automated ML Experiment"
	infoBubbleText="Running an Automated ML Experiment"
	service="microsoft.machinelearning.automl"
	resource="automl"
	authors="Aniththa"
	ms.author="anumamah"
	supportTopicIds="32690880"
	productPesIds="16644"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	articleId="microsoft.machinelearning.automl.runningexperiments"
	selfHelpType="generic"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Running an Automated ML Experiment

Here you will learn how to run an automated machine learning experiment.

## **Recommended Steps**

### Notebook

You can create an `Experiment` object, which is a named object in a `Workspace` used to run experiments:

```
from azureml.core.experiment import Experiment

ws = Workspace.from_config()

# Choose a name for the experiment and specify the project folder.
experiment_name = 'automl-classification'
project_folder = './sample_projects/automl-classification'

experiment = Experiment(ws, experiment_name)
``` 

* Submit the experiment to run and generate a model. Pass the `AutoMLConfig` to the `submit` method to generate the model: 

```
run = experiment.submit(automl_config, show_output=True)
```     

### User Interface

* Select Start to run your experiment. The experiment preparing process can take up to 10 minutes. Training jobs can take an additional 2-3 minutes more for each pipeline to finish running.

**View experiment details**

**Note**: Select **Refresh** periodically to view the status of the run. 

* The **Run Detail** screen opens to the **Details** tab. This screen shows you a summary of the experiment run including the **Run status**. 
* The **Models** tab contains a list of the models created ordered by the metric score. By default, the model that scores the highest based on the chosen metric is at the top of the list. As the training job tries out more models, they are added to the list. Use this to get a quick comparison of the metrics for the models produced so far.

## **Recommended Documents**

* [Run experiment and view results in the SDK](https://docs.microsoft.com/azure/machine-learning/how-to-configure-auto-train#run-experiment)
* [Understand automated machine learning results](https://docs.microsoft.com/azure/machine-learning/how-to-understand-automated-ml)
* [Model interpretability in automated machine learning](https://docs.microsoft.com/azure/machine-learning/how-to-machine-learning-interpretability-automl)
* [Understand automated machine learning results](https://docs.microsoft.com/azure/machine-learning/how-to-configure-auto-train#understand-automated-ml-models)
* [Create, explore, and deploy automated machine learning experiments with Azure ML UI](https://docs.microsoft.com/azure/machine-learning/how-to-use-automated-ml-for-ml-models)
* [Known Issues and Troubleshooting](https://docs.microsoft.com/azure/machine-learning/resource-known-issues#automated-machine-learning)
