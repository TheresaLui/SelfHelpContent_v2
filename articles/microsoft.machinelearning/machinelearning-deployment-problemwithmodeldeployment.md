<properties
    pageTitle="Problem with Model Deployment"
    description="Problem with Model Deployment"
    infoBubbleText="Problem with Model Deployment"
    service="microsoft.machinelearning"
    resource="deployment"
    displayOrder="1"
    authors="shivanissambare"
    ms.author="ssambare"
    articleId="machinelearning-deployment-problemwithmodeldeployment"
    selfHelpType="generic"
    supportTopicIds="32690852"
    productPesIds="16644"
    cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
    ownershipId="AzureML_AzureMachineLearningServices"
/>

# Problem with Model Deployment

Most users are able to resolve deployment issues by using the following steps.

## **Recommended Steps**

* We recommend upgrading to the latest SDK/CLI version, if you are using an old version.

1. If you encounter problems deploying a model to ACI or AKS, try deploying it as a local web service. Using a local web service makes it easier to troubleshoot problems. See Azure Machine Learning in [Deploy to Local Notebook](https://github.com/Azure/MachineLearningNotebooks/tree/master/how-to-use-azureml/deployment/deploy-to-local).

2. [Troubleshoot a failed deployment](https://docs.microsoft.com/azure/machine-learning/how-to-troubleshoot-deployment)
    * [Debug Locally](https://docs.microsoft.com/azure/machine-learning/how-to-troubleshoot-deployment#debug-locally)
    * [HTTP status code 502](https://docs.microsoft.com/azure/machine-learning/how-to-troubleshoot-deployment#http-status-code-502)
    * [HTTP status code 503](https://docs.microsoft.com/azure/machine-learning/how-to-troubleshoot-deployment#http-status-code-503)
    * [HTTP status code 504](https://docs.microsoft.com/azure/machine-learning/how-to-troubleshoot-deployment#http-status-code-504)
    * [Container cannot be scheduled error](https://docs.microsoft.com/azure/machine-learning/how-to-troubleshoot-deployment#container-cannot-be-scheduled). When deploying a service to an Azure Kubernetes Service compute target, Azure Machine Learning will attempt to schedule the service with the requested amount of resources. If there are no nodes available in the cluster with appropriate amount of resources after 5 minutes, the deployment will fail.
    * [Service launch fails](https://docs.microsoft.com/azure/machine-learning/how-to-troubleshoot-deployment#service-launch-fails). As part of container starting-up process, the init() function in your scoring script is invoked by the system. If there are uncaught error exceptions in the init() function, you might see the CrashLoopBackOff error in the error message.
    * [Function fails: get_model_path()](https://docs.microsoft.com/azure/machine-learning/how-to-troubleshoot-deployment#function-fails-get_model_path). Often, in the init() function in the scoring script, [Model.get_model_path()](https://docs.microsoft.com/python/api/azureml-core/azureml.core.model.model?view=azure-ml-py&preserve-view=true#&preserve-view=trueget-model-path-model-name--version-none---workspace-none-) function is called to locate a model file or folder of model files in the container. If the model file or folder cannot be found, the function fails.
    * [Function fails: run(input_data)](https://docs.microsoft.com/azure/machine-learning/how-to-troubleshoot-deployment#function-fails-runinput_data). If service is successfully deployed, but it crashes when you post data to the scoring endpoint, you can add error catching statement in your run(input_data).
    * [Advance Debugging](https://docs.microsoft.com/azure/machine-learning/how-to-debug-visual-studio-code#debug-and-troubleshoot-deployments). You may need to interactively debug the Python code contained in your model deployment. By using Visual Studio Code and the debugpy, you can attach to the code running inside Docker container.
    * [Webservices in Azure Kubernetes Service Failures](https://docs.microsoft.com/azure/machine-learning/resource-known-issues#webservices-in-azure-kubernetes-service-failures). Many webservice failures in Azure Kubernetes Service can be debugged by connecting to the cluster using `kubectl`.

3. [How to update a deployed web service?](https://docs.microsoft.com/azure/machine-learning/how-to-deploy-update-web-service)

4. Learn about [AKS Autoscaling in Azure Machine Learning](https://docs.microsoft.com/azure/machine-learning/how-to-deploy-azure-kubernetes-service?tabs=python#autoscaling) and [Azure ML Router](https://docs.microsoft.com/azure/machine-learning/how-to-deploy-azure-kubernetes-service?tabs=python#azure-ml-router).

5. [Limitations when deploying model to Azure Container Instances](https://docs.microsoft.com/azure/machine-learning/how-to-deploy-azure-container-instance#limitations).

6. [Advance entry script authoring](https://docs.microsoft.com/azure/machine-learning/how-to-deploy-advanced-entry-script). Learn how to write entry scripts for specialized use cases.
    * [Automatically generate a Swagger schema](https://docs.microsoft.com/azure/machine-learning/how-to-deploy-advanced-entry-script#automatically-generate-a-swagger-schema)
    * [Power BI Compatible endpoint](https://docs.microsoft.com/azure/machine-learning/how-to-deploy-advanced-entry-script#power-bi-compatible-endpoint)
    * [Binary (i.e. image) data](https://docs.microsoft.com/azure/machine-learning/how-to-deploy-advanced-entry-script#binary-data)
    * [Cross-origin resource sharing (CORS)](https://docs.microsoft.com/azure/machine-learning/how-to-deploy-advanced-entry-script#cross-origin-resource-sharing-cors)
    * [Framework specific examples](https://docs.microsoft.com/azure/machine-learning/how-to-deploy-advanced-entry-script#framework-specific-examples). More entry script examples for specific machine learning use cases (PyTorch, TensorFlow, Keras, AutoML, ONNX).

7. Learn how to [Load Registered models](https://docs.microsoft.com/azure/machine-learning/how-to-deploy-advanced-entry-script#load-registered-models). There are two ways to locate models in your entry script.

8. [Secure an Azure Machine Learning Inferencing environment with virtual networks](https://docs.microsoft.com/azure/machine-learning/how-to-secure-inferencing-vnet?tabs=python)
    * [Learn about network requirements that must be met to use an AKS cluster in a virtual network](https://docs.microsoft.com/azure/machine-learning/how-to-secure-inferencing-vnet?tabs=python#azure-kubernetes-service)
    * [Network Contributor Role](https://docs.microsoft.com/azure/machine-learning/how-to-secure-inferencing-vnet?tabs=python#network-contributor-role)
    * [Secure VNet Traffic](https://docs.microsoft.com/azure/machine-learning/how-to-secure-inferencing-vnet?tabs=python#secure-vnet-traffic). There are two ways to isolate traffic to and from AKS cluster to the virtual network. [Private AKS cluster](https://docs.microsoft.com/azure/machine-learning/how-to-secure-inferencing-vnet?tabs=python#private-aks-cluster) and [Internal AKS Load Balancer](https://docs.microsoft.com/azure/machine-learning/how-to-secure-inferencing-vnet?tabs=python#internal-aks-load-balancer)
    * [To enable Azure Machine Learning to create ACI inside the virtual network, you must enable subnet delegation for the subnet used by the deployment](https://docs.microsoft.com/azure/machine-learning/how-to-secure-inferencing-vnet?tabs=python#enable-azure-container-instances-aci)
    * [Limit outbound connectivity from the virtual network](https://docs.microsoft.com/azure/machine-learning/how-to-secure-inferencing-vnet?tabs=python#limit-outbound-connectivity-from-the-virtual-network)
    * [Understand connectivity requirements for AKS inferencing cluster](https://docs.microsoft.com/azure/machine-learning/how-to-deploy-azure-kubernetes-service?tabs=python#understand-connectivity-requirements-for-aks-inferencing-cluster)

9. [Create and attach an Azure Kubernetes Service cluster.](https://docs.microsoft.com/azure/machine-learning/how-to-create-attach-kubernetes?tabs=python)
    * [Prerequisites](https://docs.microsoft.com/azure/machine-learning/how-to-create-attach-kubernetes?tabs=python#prerequisites)
    * [Limitations](https://docs.microsoft.com/azure/machine-learning/how-to-create-attach-kubernetes?tabs=python#limitations)
    * [Azure Kubernetes Service version](https://docs.microsoft.com/azure/machine-learning/how-to-create-attach-kubernetes?tabs=python#azure-kubernetes-service-version)

**Python SDK**

* [Webservice Package](https://docs.microsoft.com/python/api/azureml-core/azureml.core.webservice?view=azure-ml-py) contains functionality for deploying machine learning models as web service endpoints in Azure Machine Learning.
* [AksWebService class](https://docs.microsoft.com/python/api/azureml-core/azureml.core.webservice.akswebservice?view=azure-ml-py&preserve-view=true)
* [AciWebService class](https://docs.microsoft.com/python/api/azureml-core/azureml.core.webservice.aciwebservice?view=azure-ml-py)
* [SSL configuration class](https://docs.microsoft.com/python/api/azureml-core/azureml.core.compute.aks.sslconfiguration?view=azure-ml-py)
* [AksProvisioningConfiguration.enable_ssl()](https://docs.microsoft.com/python/api/azureml-core/azureml.core.compute.aks.aksprovisioningconfiguration?view=azure-ml-py#enable-ssl-ssl-cname-none--ssl-cert-pem-file-none--ssl-key-pem-file-none--leaf-domain-label-none--overwrite-existing-domain-false-)
* [AksAttachConfiguration.enable_ssl()](https://docs.microsoft.com/python/api/azureml-core/azureml.core.compute.aks.aksattachconfiguration?view=azure-ml-py#enable-ssl-ssl-cname-none--ssl-cert-pem-file-none--ssl-key-pem-file-none--leaf-domain-label-none--overwrite-existing-domain-false-)

**How to**

* [Secure the Inferencing environment](https://docs.microsoft.com/azure/machine-learning/how-to-network-security-overview#secure-the-inferencing-environment)
* [Use TLS to secure a web service through Azure Machine Learning](https://docs.microsoft.com/azure/machine-learning/how-to-secure-web-service)
* [How to use your workspace with a custom DNS server](https://docs.microsoft.com/azure/machine-learning/how-to-custom-dns?tabs=azure-cli)
* [Network isolation with private virtual networks](https://docs.microsoft.com/azure/machine-learning/how-to-enable-virtual-network#azure-kubernetes-service)
* [Use Azure AD identity with your machine learning web service in Azure Kubernetes Service](https://docs.microsoft.com/azure/machine-learning/how-to-use-azure-ad-identity)
* [Set up Web-service authentication](https://docs.microsoft.com/azure/machine-learning/how-to-setup-authentication#web-service-authentication)

**Helpful articles**

* [How to package a registered model with Docker?](https://docs.microsoft.com/azure/machine-learning/how-to-deploy-package-models) Learn how to package a registered Azure Machine Learning model with Docker.
* [Use the studio to deploy models trained in the Designer](https://docs.microsoft.com/azure/machine-learning/how-to-deploy-model-designer). Learn how to deploy trained model from Designer as a real-time endpoint in Azure Machine Learning Studio.
* [Profile your model to determine resource utilization.](https://docs.microsoft.com/azure/machine-learning/how-to-deploy-profile-model?pivots=py-sdk)
* [InferenceSchema](https://github.com/Azure/InferenceSchema) This Python package is intended to provide uniform schema for common machine learning applications, as well as a set of decorators that can be used to aid in web-based ML prediction applications.
* [ONNX and Azure Machine Learning: Create and accelerate ML models.](https://docs.microsoft.com/azure/machine-learning/concept-onnx)

## **Recommended Documents**

* [Deploy models with Azure Machine Learning](https://docs.microsoft.com/azure/machine-learning/how-to-deploy-and-where)
* [Deploy model to an Azure Kubernetes Service cluster](https://docs.microsoft.com/azure/machine-learning/how-to-deploy-azure-kubernetes-service)
* [Deploy a model to Azure Container Instances](https://docs.microsoft.com/azure/machine-learning/how-to-deploy-azure-container-instance)
* [Deploy a high-performance scoring endpoint with Triton](https://docs.microsoft.com/azure/machine-learning/how-to-deploy-with-triton?tabs=pythons)
