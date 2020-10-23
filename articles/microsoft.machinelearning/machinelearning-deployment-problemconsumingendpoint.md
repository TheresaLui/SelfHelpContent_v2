<properties
    pageTitle="Problem Consuming Endpoint"
    description="Problem Consuming Endpoint"
    infoBubbleText="Problem Consuming Endpoint"
    resource="deployment"
    displayOrder="1"
    authors="shivanissambare"
    ms.author="ssambare"
    articleId="machinelearning-deployment-problemconsumingendpoint"
    selfHelpType="generic"
    supportTopicIds="32690875"
    productPesIds="16644"
    cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
    ownershipId="AzureML_AzureMachineLearningServices"
/>

# Problem Consuming Endpoint

Most users are able to resolve this issue using the steps below.

## **Recommended Steps**

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

* [Collect and evaluate model data](https://docs.microsoft.com/azure/machine-learning/how-to-enable-data-collection)
* [Monitor and collect data from ML web service endpoints](https://docs.microsoft.com/azure/machine-learning/how-to-enable-app-insights)
* If you encounter problems deploying a model to ACI or AKS, try deploying it as a local web service. Using a local web service makes it easier to troubleshoot problems.
* [Troubleshoot and Debugging Guide](https://docs.microsoft.com/azure/machine-learning/how-to-troubleshoot-deployment)
* You can also refer to Azure Machine Learning - [Deploy to Local Notebook](https://github.com/Azure/MachineLearningNotebooks/tree/master/how-to-use-azureml/deployment/deploy-to-local)

## **Recommended Documents**

* [Deploy models with Azure Machine Learning](https://docs.microsoft.com/azure/machine-learning/how-to-deploy-and-where)
* [Deploy model to an Azure Kubernetes Service cluster](https://docs.microsoft.com/azure/machine-learning/how-to-deploy-azure-kubernetes-service)
* [Deploy a model to Azure Container Instances](https://docs.microsoft.com/azure/machine-learning/how-to-deploy-azure-container-instance)

**Python SDK**

[Webservice Package](https://docs.microsoft.com/python/api/azureml-core/azureml.core.webservice?view=azure-ml-py) contains functionality for deploying machine learning models as web service endpoints in Azure Machine Learning.
[AksWebService class](https://docs.microsoft.com/python/api/azureml-core/azureml.core.webservice.akswebservice?view=azure-ml-py&preserve-view=true)
[AciWebService class](https://docs.microsoft.com/python/api/azureml-core/azureml.core.webservice.aciwebservice?view=azure-ml-py)

**Enterprise Readiness and Security**

* [Use TLS to secure a web service through Azure Machine Learning](https://docs.microsoft.com/azure/machine-learning/how-to-secure-web-service)
* [How to use your workspace with a custom DNS server](https://docs.microsoft.com/azure/machine-learning/how-to-custom-dns?tabs=azure-cli)
* [Secure the Inferencing environment](https://docs.microsoft.com/azure/machine-learning/how-to-network-security-overview#secure-the-inferencing-environment)
* [Secure an Azure Machine Learning inferencing environment with virtual networks](https://docs.microsoft.com/azure/machine-learning/how-to-secure-inferencing-vnet?tabs=python)
* [Network isolation with private virtual networks](https://docs.microsoft.com/azure/machine-learning/how-to-enable-virtual-network#azure-kubernetes-service)
* [Use Azure AD identity with your machine learning web service in Azure Kubernetes Service](https://docs.microsoft.com/azure/machine-learning/how-to-use-azure-ad-identity)
* [Set up Web-service authentication](https://docs.microsoft.com/azure/machine-learning/how-to-setup-authentication#web-service-authentication)
