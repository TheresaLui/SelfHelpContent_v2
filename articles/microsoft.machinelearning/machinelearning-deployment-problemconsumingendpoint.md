<properties
    pageTitle="Problem Consuming Endpoint (web services)"
    description="Problem Consuming Endpoint (web services)"
    infoBubbleText="Problem Consuming Endpoint (web services)"
    service="microsoft.machinelearning"
    resource="deployment"
    authors="shivanissambare"
    ms.author="ssambare"
    displayOrder="1"
    articleId="machinelearning-deployment-problemconsumingendpoint"
    selfHelpType="generic"
    supportTopicIds="32690875"
    productPesIds="16644"
    cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
    ownershipId="AzureML_AzureMachineLearningServices"
/>

# Problem Consuming Endpoint (web services)

Most users are able to resolve this issue using the steps below.

## **Recommended Steps**

* Refer to [Consume an Azure Machine Learning model deployed as a web service](https://docs.microsoft.com/azure/machine-learning/how-to-consume-web-service)
* If you encounter problems deploying a model to ACI or AKS, try deploying it as a local web service. Using a local web service makes it easier to troubleshoot problems. [Troubleshoot and Debugging Guide](https://docs.microsoft.com/azure/machine-learning/how-to-troubleshoot-deployment)
* You can also refer to Azure Machine Learning - [Deploy to Local Notebook](https://github.com/Azure/MachineLearningNotebooks/tree/master/how-to-use-azureml/deployment/deploy-to-local)

## **Recommended Documents**

* [Deploy models with Azure Machine Learning](https://docs.microsoft.com/azure/machine-learning/how-to-deploy-and-where)
* [Deploy a model to an Azure Kubernetes Service cluster](https://docs.microsoft.com/azure/machine-learning/how-to-deploy-azure-kubernetes-service)
* [Deploy a model to Azure Container Instances](https://docs.microsoft.com/azure/machine-learning/how-to-deploy-azure-container-instance)

**Python SDK**

[Webservice Package](https://docs.microsoft.com/python/api/azureml-core/azureml.core.webservice?view=azure-ml-py) contains functionality for deploying machine learning models as web service endpoints in Azure Machine Learning.

**Enterprise Readiness and Security**

* [Use TLS to secure a web service through Azure Machine Learning](https://docs.microsoft.com/azure/machine-learning/how-to-secure-web-service)
* [Network isolation with private virtual networks](https://docs.microsoft.com/azure/machine-learning/how-to-enable-virtual-network#azure-kubernetes-service)
* [Use Azure AD identity with your machine learning web service in Azure Kubernetes Service](https://docs.microsoft.com/azure/machine-learning/how-to-use-azure-ad-identity)
* [Set up Web-service authentication](https://docs.microsoft.com/azure/machine-learning/how-to-use-azure-ad-identity)