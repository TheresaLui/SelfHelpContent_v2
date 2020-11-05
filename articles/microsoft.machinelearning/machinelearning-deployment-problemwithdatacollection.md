<properties
    pageTitle="Problem with Data Collection for models or web service"
    description="Problem with Data Collection for models or web service"
    infoBubbleText="Problem with Data Collection for models or web service"
    service="microsoft.machinelearning"
    resource="deployment"
    displayOrder="1"
    authors="shivanissambare"
    ms.author="ssambare"
    articleId="machinelearning-deployment-problemwithdatacollection"
    selfHelpType="generic"
    supportTopicIds="32690850"
    productPesIds="16644"
    cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
    ownershipId="AzureML_AzureMachineLearningServices"
/>

# Problem with Data Collection for models or web service

Most users are able to resolve this issue using the steps below.

## **Recommended Steps**

* Refer to [Collect and evaluate model data](https://docs.microsoft.com/azure/machine-learning/how-to-enable-data-collection)

* Refer to [Monitor and collect data from ML web service endpoints](https://docs.microsoft.com/azure/machine-learning/how-to-enable-app-insights)

* Refer to [Consume an Azure Machine Learning model deployed as a web service](https://docs.microsoft.com/azure/machine-learning/how-to-consume-web-service). Deploying an Azure Machine Learning model as web service creates REST API endpoint. You can send data to this endpoint and receive the prediction returned by the model. In this article, learn how to create clients for the web service by using C#, Go, Java, and Python.

* [Consume the service from Power BI](https://docs.microsoft.com/azure/machine-learning/how-to-consume-web-service?tabs=python#consume-the-service-from-power-bi). Once the web service is deployed, it's consumable from Power BI dataflows. [Learn how to consume an Azure Machine Learning web service from Power BI.](https://docs.microsoft.com/power-bi/transform-model/dataflows/dataflows-machine-learning-integration)

* [How to update a deployed web service?](https://docs.microsoft.com/azure/machine-learning/how-to-deploy-update-web-service)

* [Advance Entry Script Authoring](https://docs.microsoft.com/azure/machine-learning/how-to-deploy-advanced-entry-script). This article shows how to write entry scripts for specialized use case:

    * [Automatically generate a Swagger schema](https://docs.microsoft.com/azure/machine-learning/how-to-deploy-advanced-entry-script#automatically-generate-a-swagger-schema)
    * [Power BI Compatible endpoint](https://docs.microsoft.com/azure/machine-learning/how-to-deploy-advanced-entry-script#power-bi-compatible-endpoint)
    * [Binary (i.e. image) data](https://docs.microsoft.com/azure/machine-learning/how-to-deploy-advanced-entry-script#binary-data)
    * [Cross-origin resource sharing (CORS)](https://docs.microsoft.com/azure/machine-learning/how-to-deploy-advanced-entry-script#cross-origin-resource-sharing-cors)
    * [Load Registered models](https://docs.microsoft.com/azure/machine-learning/how-to-deploy-advanced-entry-script#load-registered-models). There are two ways to locate models in your entry script.
    * [Framework specific examples](https://docs.microsoft.com/azure/machine-learning/how-to-deploy-advanced-entry-script#framework-specific-examples). More entry script examples for specific machine learning use cases (PyTorch, TensorFlow, Keras, AutoML, ONNX).

* [InferenceSchema](https://github.com/Azure/InferenceSchema) This Python package is intended to provide uniform schema for common machine learning applications, as well as a set of decorators that can be used to aid in web-based ML prediction applications.

* [Collect and evaluate model data](https://docs.microsoft.com/azure/machine-learning/how-to-enable-data-collection)

* [Monitor and collect data from ML web service endpoints](https://docs.microsoft.com/azure/machine-learning/how-to-enable-app-insights)

* [Troubleshoot a failed deployment](https://docs.microsoft.com/azure/machine-learning/how-to-troubleshoot-deployment)

    * [Debug Locally](https://docs.microsoft.com/azure/machine-learning/how-to-troubleshoot-deployment#debug-locally)

    * [HTTP status code 502](https://docs.microsoft.com/azure/machine-learning/how-to-troubleshoot-deployment#http-status-code-502)

    * [HTTP status code 503](https://docs.microsoft.com/azure/machine-learning/how-to-troubleshoot-deployment#http-status-code-503)

    * [HTTP status code 504](https://docs.microsoft.com/azure/machine-learning/how-to-troubleshoot-deployment#http-status-code-504)

    * [Container cannot be scheduled error](https://docs.microsoft.com/azure/machine-learning/how-to-troubleshoot-deployment#container-cannot-be-scheduled). When deploying a service to an Azure Kubernetes Service compute target, Azure Machine Learning will attempt to schedule the service with the requested amount of resources. If there are no nodes available in the cluster with appropriate amount of resources after 5 minutes, the deployment will fail.

    * [Service launch fails](https://docs.microsoft.com/azure/machine-learning/how-to-troubleshoot-deployment#service-launch-fails). As part of container starting-up process, the init() function in your scoring script is invoked by the system. If there are uncaught error exceptions in the init() function, you might see CrashLoopBackOff error in the error message.

    * [Function fails: get_model_path()](https://docs.microsoft.com/azure/machine-learning/how-to-troubleshoot-deployment#function-fails-get_model_path). Often, in the init() function in the scoring script, [Model.get_model_path()](https://docs.microsoft.com/python/api/azureml-core/azureml.core.model.model?view=azure-ml-py&preserve-view=true#&preserve-view=trueget-model-path-model-name--version-none---workspace-none-) function is called to locate a model file or folder of model files in the container. If the model file or folder cannot be found, the function fails.

    * [Function fails: run(input_data)](https://docs.microsoft.com/azure/machine-learning/how-to-troubleshoot-deployment#function-fails-runinput_data). If service is successfully deployed, but it crashes when you post data to the scoring endpoint, you can add error catching statement in your run(input_data).

    * [Advance Debugging](https://docs.microsoft.com/azure/machine-learning/how-to-debug-visual-studio-code#debug-and-troubleshoot-deployments). You may need to interactively debug the Python code contained in your model deployment. By using Visual Studio Code and the debugpy, you can attach to the code running inside Docker container.

    * [Webservices in Azure Kubernetes Service Failures](https://docs.microsoft.com/azure/machine-learning/resource-known-issues#webservices-in-azure-kubernetes-service-failures). Many webservice failures in Azure Kubernetes Service can be debugged by connecting to the cluster using `kubectl`.

## **Recommended Documents**

* [Deploy models with Azure Machine Learning](https://docs.microsoft.com/azure/machine-learning/how-to-deploy-and-where)
* [Deploy model to an Azure Kubernetes Service cluster](https://docs.microsoft.com/azure/machine-learning/how-to-deploy-azure-kubernetes-service)
* [Deploy a model to Azure Container Instances](https://docs.microsoft.com/azure/machine-learning/how-to-deploy-azure-container-instance)
* [InferenceSchema](https://github.com/Azure/InferenceSchema) This Python package is intended to provide uniform schema for common machine learning applications, as well as a set of decorators that can be used to aid in web-based ML prediction applications.
* Understand [AKS Autoscaling in Azure Machine Learning](https://docs.microsoft.com/azure/machine-learning/how-to-deploy-azure-kubernetes-service?tabs=python#autoscaling) and [Azure ML Router](https://docs.microsoft.com/azure/machine-learning/how-to-deploy-azure-kubernetes-service?tabs=python#azure-ml-router).

**Python SDK**

* [Webservice Package](https://docs.microsoft.com/python/api/azureml-core/azureml.core.webservice?view=azure-ml-py) contains functionality for deploying machine learning models as web service endpoints in Azure Machine Learning.

**Enterprise Readiness and Security**

* [Use TLS to secure a web service through Azure Machine Learning](https://docs.microsoft.com/azure/machine-learning/how-to-secure-web-service)
* [Network isolation with private virtual networks](https://docs.microsoft.com/azure/machine-learning/how-to-enable-virtual-network#azure-kubernetes-service)
* [Use Azure AD identity with your machine learning web service in Azure Kubernetes Service](https://docs.microsoft.com/azure/machine-learning/how-to-use-azure-ad-identity)
* [Set up Web-service authentication](https://docs.microsoft.com/azure/machine-learning/how-to-use-azure-ad-identity)
