<properties
	pageTitle="Problem deploying real-time endpoint in the designer"
	description="Problem deploying real-time endpoint in the designer"
	infoBubbleText="Problem deploying real-time endpoint in the designer"
	service="microsoft.machinelearning"
	resource="designer"
	authors="likebupt"
	ms.author="keli19"
	articleId="machine-learning-designer-problem-deploy-real-time-endpoint"
	selfHelpType="generic"
	supportTopicIds="32789517"
	productPesIds="16644"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Problem deploying real-time endpoint in the designer

## **Recommended Steps**

* Create real-time inference pipeline
  - If you training pipeline contains more than one **Train Model** module, please select one **Train Model** module when you create real-time inference pipeline. Real-time inference pipeline can only contain one trained model.
  - If your training pipeline contains **Extract N-Gram Features from Text** module, you need to manually adjust your inference pipeline. See details in the [module article](https://docs.microsoft.com/azure/machine-learning/algorithm-module-reference/extract-n-gram-features-from-text#build-inference-pipeline-that-uses-n-grams-to-deploy-a-real-time-endpoint).

* Deployment failure

    When you have finished deployment setting in the designer and deployment start, You can check the **Deployment logs** in the real-time endpoint detail page.

* Test or consume real-time endpoint

    If your pipeline contains **Execute Python Script** or **Execute R Script** which produces multiple row data, please note that the real-time endpoint expects one row data from web service input. 
    If you want to predict multiple row data, you can refer refer to [this article](https://docs.microsoft.com/azure/machine-learning/how-to-run-batch-predictions-designer) to learn how to run batch predictions in the designer. 

## **Recommended Documents**

* [What is Azure Machine Learning designer?](https://docs.microsoft.com/azure/machine-learning/concept-designer)
* [Retrain models using pipeline parameter in the designer](https://docs.microsoft.com/azure/machine-learning/how-to-retrain-designer)
* [Run batch predictions using pipeline parameter in the designer](https://docs.microsoft.com/azure/machine-learning/how-to-run-batch-predictions-designer)
* [Publish pipeline and consume pipeline endpoint using SDK](https://docs.microsoft.com/azure/machine-learning/how-to-deploy-pipelines)