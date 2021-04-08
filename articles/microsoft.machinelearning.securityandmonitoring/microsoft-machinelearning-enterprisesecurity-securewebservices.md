<properties
	pageTitle="Secure Web Services"
	description="Secure Web Services"
	infoBubbleText="Secure Web Services"
	service="microsoft.machinelearning"
	resource="machinelearning"
	authors="johnwu0604"
	ms.author="johwu"
	supportTopicIds="32690883"
	productPesIds="16644"
	cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
	articleId="microsoft.machinelearning.enterprisesecurity.securewebservices"
	selfHelpType="generic"
	ownershipId="AzureML_AzureMachineLearningServices"
/>

# Secure Web Services 

[Troubleshooting and Debugging Guide](https://docs.microsoft.com/azure/machine-learning/how-to-troubleshoot-deployment?tabs=azcli)

## **Recommended Steps**

There are two steps you should take to secure your web services:

1. Ensure you have SSL enabled on your web service domain.
2. Ensure you have either key-based or token-based authentication enabled on your scoring endpoint.

### **Set up SSL**

The general process to secure a web service using SSL is as follows:

1. Get a domain name
2. Get a digital certificate
3. Deploy or update the web service with SSL enabled
4. Update your DNS to point to the web service

The [following article](https://docs.microsoft.com/azure/machine-learning/how-to-secure-web-service) covers this process in depth.

### **Set up Key-based Authentication**

Key-based authentication generates static bearer-type authentication keys that do not need to be refreshed. 

* Key-based authentication is **enabled by default** when you deploy to Azure Kubernetes Service
* Key-based authentication is **disabled by default** when you deploy to Azure Container Instances, but you can enable it by setting `auth_enabled=True` when creating the ACI web-service

The following is an example of creating an ACI deployment configuration with key-based authentication enabled:

```
from azureml.core.webservice import AciWebservice

aci_config = AciWebservice.deploy_configuration(cpu_cores=1,
                                                memory_gb=1,
                                                auth_enable=True)									
```

Then you can use the custom ACI configuration in deployment using the `Model` class:

```
from azureml.core.model import Model, InferenceConfig

inference_config = InferenceConfig(entry_script='score.py',
                                   environment=myenv)
aci_service = Model.deploy(workspace=ws,
						   name='aci_service_sample',
						   models=[model],
						   inference_config=inference_config,
						   deployment_config=aci_config)
aci_service.wait_for_deployment(True)
```

To consume the web service, use `aci_service.get_keys()` to fetch the key and set this in the authorization header:

```
import requests
import json

headers = {'Content-Type': 'application/json'}
headers['Authorization'] = 'Bearer '+ aci_service.get_keys()[0]

test_sample = json.dumps({'data': [
    [1, 2, 3, 4, 5, 6, 7, 8, 9, 10],
    [10, 9, 8, 7, 6, 5, 4, 3, 2, 1]
]})

response = requests.post(aci_service.scoring_uri, data=test_sample, headers=headers)
```

To regenerate a key, use the `regen_key()` function and pass either **Primary** or **Secondary**:

`aci_service.regen_key('Primary')` or `aci_service.regen_key('Secondary')`

### **Set up Token-based Authentication**

Token-based authentication requires users to present an Azure Machine Learning JSON Web Token to the web service to access it. The token expires after a specified time-frame and needs to be refreshed to continue making calls.

* Token authentication is disabled by default when you deploy to Azure Kubernetes Service
* Token authentication isn't supported when you deploy to Azure Container Instances

To control token authentication, use the `token_auth_enabled` parameter when you create or update a deployment.

The following is an example of creating an AKS deployment configuration with token-based authentication enabled:

```
from azureml.core.webservice import AksWebservice

aks_config = AksWebservice.deploy_configuration(cpu_cores=1,
                                                memory_gb=1,
                                                token_auth_enabled=True)
```

Then, you can use the custom AKS configuration in deployment using the `Model` class:

```
from azureml.core.model import Model, InferenceConfig

inference_config = InferenceConfig(entry_script='score.py',
                                   environment=myenv)
aks_service = Model.deploy(workspace=ws,
						   name='aks_service_sample',
						   models=[model],
						   inference_config=inference_config,
						   deployment_config=aks_config)
aks_service.wait_for_deployment(True)
```

To consume the web service, use the `aks_service.get_access_token()` method to retrieve a JSON Web Token (JWT) and set this in the authorization header:

```
import requests
import json

token, refresh_by = aks_service.get_token()

headers = {'Content-Type': 'application/json'}
headers['Authorization'] = 'Bearer '+ token

test_sample = json.dumps({'data': [
    [1, 2, 3, 4, 5, 6, 7, 8, 9, 10],
    [10, 9, 8, 7, 6, 5, 4, 3, 2, 1]
]})

response = requests.post(aks_service.scoring_uri, data=test_sample, headers=headers)
```

You'll need to request a new token after the token's `refresh_by` time.

## **Recommended Documents**

Here is a list of additional resources which may be helpful: 

* [SSL configuration class](https://docs.microsoft.com/python/api/azureml-core/azureml.core.compute.aks.sslconfiguration?view=azure-ml-py)
* [AksProvisioningConfiguration.enable_ssl()](https://docs.microsoft.com/python/api/azureml-core/azureml.core.compute.aks.aksprovisioningconfiguration?view=azure-ml-py#enable-ssl-ssl-cname-none--ssl-cert-pem-file-none--ssl-key-pem-file-none--leaf-domain-label-none--overwrite-existing-domain-false-)
* [AksAttachConfiguration.enable_ssl()](https://docs.microsoft.com/python/api/azureml-core/azureml.core.compute.aks.aksattachconfiguration?view=azure-ml-py#enable-ssl-ssl-cname-none--ssl-cert-pem-file-none--ssl-key-pem-file-none--leaf-domain-label-none--overwrite-existing-domain-false-)
* [Set up authentication for Azure Machine Learning resources and workflows](https://docs.microsoft.com/azure/machine-learning/how-to-setup-authentication)
* [Consume an Azure Machine Learning model deployed as a web service](https://docs.microsoft.com/azure/machine-learning/how-to-consume-web-service)
* [Azure Machine Learning SDK documentation](https://docs.microsoft.com/python/api/overview/azure/ml/?view=azure-ml-py)

* [Secure an Azure Machine Learning Inferencing environment with virtual networks](https://docs.microsoft.com/azure/machine-learning/how-to-secure-inferencing-vnet?tabs=python)
    * [Learn about network requirements that must be met to use an AKS cluster in a virtual network](https://docs.microsoft.com/azure/machine-learning/how-to-secure-inferencing-vnet?tabs=python#azure-kubernetes-service)
    * [Network Contributor Role](https://docs.microsoft.com/azure/machine-learning/how-to-secure-inferencing-vnet?tabs=python#network-contributor-role)
    * [Secure VNet Traffic](https://docs.microsoft.com/azure/machine-learning/how-to-secure-inferencing-vnet?tabs=python#secure-vnet-traffic). There are two ways to isolate traffic to and from AKS cluster to the virtual network. [Private AKS cluster](https://docs.microsoft.com/azure/machine-learning/how-to-secure-inferencing-vnet?tabs=python#private-aks-cluster) and [Internal AKS Load Balancer](https://docs.microsoft.com/azure/machine-learning/how-to-secure-inferencing-vnet?tabs=python#internal-aks-load-balancer)
    * [To enable Azure Machine Learning to create ACI inside the virtual network, you must enable subnet delegation for the subnet used by the deployment](https://docs.microsoft.com/azure/machine-learning/how-to-secure-inferencing-vnet?tabs=python#enable-azure-container-instances-aci)
    * [Limit outbound connectivity from the virtual network](https://docs.microsoft.com/azure/machine-learning/how-to-secure-inferencing-vnet?tabs=python#limit-outbound-connectivity-from-the-virtual-network)

**How to**

* [Secure the Inferencing environment](https://docs.microsoft.com/azure/machine-learning/how-to-network-security-overview#secure-the-inferencing-environment)
* [Use TLS to secure a web service through Azure Machine Learning](https://docs.microsoft.com/azure/machine-learning/how-to-secure-web-service)
* [How to use your workspace with a custom DNS server](https://docs.microsoft.com/azure/machine-learning/how-to-custom-dns?tabs=azure-cli)
* [Network isolation with private virtual networks](https://docs.microsoft.com/azure/machine-learning/how-to-enable-virtual-network#azure-kubernetes-service)
* [Use Azure AD identity with your machine learning web service in Azure Kubernetes Service](https://docs.microsoft.com/azure/machine-learning/how-to-use-azure-ad-identity)
* [Set up Web-service authentication](https://docs.microsoft.com/azure/machine-learning/how-to-setup-authentication#web-service-authentication)
