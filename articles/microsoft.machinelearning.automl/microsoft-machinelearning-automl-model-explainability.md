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

From this article, learn how to resolve problems with model explainability in automated machine learning. 

- In all SDK versions after 1.0.85, model interpretability is enabled by default (`model_explainability=True`)
- In SDK version 1.0.85 and earlier, model interpretability has to be set manually (set `model_explainability=True` in the `AutoMLConfig` object) 

## ValueError: Feature vector length mismatch: feature names length differs from local explanations dimension
This error occurs if the features in `x_test` don't match the features in the training data used to train the model. Make sure that both use the same features. AutoML supports explanations for both raw and engineered features. 

- For engineered explanations, pass the engineered data as `datasetX`:

  `ExplanationDashboard(raw_explanations, automl_explainer_setup_obj.automl_pipeline, datasetX=automl_explainer_setup_obj.X_test_raw)`

- For raw explanations, pass raw data as `datasetX`:

   `ExplanationDashboard(engineered_explanations, automl_explainer_setup_obj.automl_estimator, datasetX=automl_explainer_setup_obj.X_test_transform)`

## **Recommended Documents**

* [Interpretability: model explanations in automated machine learning (preview)](https://docs.microsoft.com/azure/machine-learning/how-to-machine-learning-interpretability-automl)
* [Model interpretability in Azure Machine Learning](https://docs.microsoft.com/azure/machine-learning/how-to-machine-learning-interpretability)
* [Known Issues and Troubleshooting](https://docs.microsoft.com/azure/machine-learning/resource-known-issues#automated-machine-learning)
