<properties
	pageTitle="SSL setup for ACI or AKS"
	description="SSL setup for ACI or AKS"
	infoBubbleText="SSL setup for ACI or AKS"
	service="microsoft.machinelearning"
	resource="machinelearning"
	authors="johnwu0604"
	ms.author="johwu"
	supportTopicIds="32690883"
	productPesIds="16644"
	cloudEnvironments="Public"
	articleId="microsoft.machinelearning.securityandmonitoring.ssl"
	selfHelpType="generic"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# SSL setup for ACI or AKS

## **Recommended Steps**

The general process to secure a web service using SSL is as follows:

1. Get a domain name
2. Get a digital certificate
3. Deploy or update the web service with SSL enabled
4. Update your DNS to point to the web service

The [following article](https://docs.microsoft.com/azure/machine-learning/how-to-secure-web-service) covers this process in depth.

## **Recommended Documents**

Here is a list of additional resources which may be helpful:

* [SSL configuration class](https://docs.microsoft.com/python/api/azureml-core/azureml.core.compute.aks.sslconfiguration?view=azure-ml-py)
* [AksProvisioningConfiguration.enable_ssl()](https://docs.microsoft.com/python/api/azureml-core/azureml.core.compute.aks.aksprovisioningconfiguration?view=azure-ml-py#enable-ssl-ssl-cname-none--ssl-cert-pem-file-none--ssl-key-pem-file-none--leaf-domain-label-none--overwrite-existing-domain-false-)
* [AksAttachConfiguration.enable_ssl()](https://docs.microsoft.com/python/api/azureml-core/azureml.core.compute.aks.aksattachconfiguration?view=azure-ml-py#enable-ssl-ssl-cname-none--ssl-cert-pem-file-none--ssl-key-pem-file-none--leaf-domain-label-none--overwrite-existing-domain-false-)
* [Azure Machine Learning SDK documentation](https://docs.microsoft.com/python/api/overview/azure/ml/?view=azure-ml-py)
