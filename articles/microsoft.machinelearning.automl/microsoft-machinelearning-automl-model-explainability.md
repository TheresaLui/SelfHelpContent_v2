<properties
  pagetitle="Problem with Model Explainability with Automated Machine Learning"
  service="microsoft.machinelearning.automl"
  resource="automl"
  ms.author="anumamah,mithigpe"
  selfhelptype="Generic"
  supporttopicids="32755242"
  resourcetags=""
  productpesids="16644"
  cloudenvironments="public,fairfax,mooncake,usnat,ussec"
  articleid="microsoft.machinelearning.automl.modelexplainability"
  ownershipid="AzureML_AzureMachineLearningServices" />
# Problem with Model Explainability with Automated Machine Learning

In this article, you learn how to resolve automated machine learning related model explainability.

All SDK versions after 1.0.85 set model_explainability=True by default. 
In SDK version 1.0.85 and earlier versions users need to set model_explainability=True in the AutoMLConfig object in order to use model interpretability.

## ValueError: Feature vector length mismatch: feature names length differs from local explanations dimension
User will get this error if the features in x_test doesn't match with the features in the training data which was used to train the model. Please ensure if the same features are used. AutoML supports explanations for both raw and engineered features. For engineered explanations user should pass the engineered data as datasetX:

    ExplanationDashboard(raw_explanations, automl_explainer_setup_obj.automl_pipeline, datasetX=automl_explainer_setup_obj.X_test_raw)

and for raw explanations they should pass raw data as datasetX:

    ExplanationDashboard(engineered_explanations, automl_explainer_setup_obj.automl_estimator, datasetX=automl_explainer_setup_obj.X_test_transform)

## **Recommended Documents**

* [Interpretability: model explanations in automated machine learning (preview)](https://docs.microsoft.com/azure/machine-learning/how-to-machine-learning-interpretability-automl)
* [Model interpretability in Azure Machine Learning](https://docs.microsoft.com/azure/machine-learning/how-to-machine-learning-interpretability)
* [Known Issues and Troubleshooting](https://docs.microsoft.com/azure/machine-learning/resource-known-issues#automated-machine-learning)