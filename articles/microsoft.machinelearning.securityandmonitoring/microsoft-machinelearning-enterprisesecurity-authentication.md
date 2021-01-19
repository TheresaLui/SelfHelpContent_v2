<properties
  pagetitle="Authentication Issues&#xD;"
  service="microsoft.machinelearning"
  resource="machinelearning"
  ms.author="johwu"
  selfhelptype="Generic"
  supporttopicids="32690837"
  resourcetags=""
  productpesids="16644"
  cloudenvironments="public,fairfax,mooncake,usnat,ussec"
  articleid="microsoft.machinelearning.enterprisesecurity.authentication"
  ownershipid="AzureML_AzureMachineLearningServices" />
# Authentication Issues

## **Recommended Steps**

### **Interactive authentication**

Most examples in our documentation use interactive authentication, which uses your account in Azure AD to directly authenticate. You can do this by using Azure Machine Learning [Python SDK](https://docs.microsoft.com/python/api/overview/azure/ml/?view=azure-ml-py), as follows: 

```
from azureml.core import Workspace
workspace = Workspace(subscription_id="<YOUR_SUBSCRIPTION_ID",
                      resource_group="<YOUR_RESOURCE_GROUP>",
                      workspace_name="<YOUR_WORKSPACE_NAME")
workspace.get_details()
```

The preceding function call will prompt you with a UI-based authentication flow.

### **Authenticate through automated workflows**

Service principal authentication can be used to authentication through automated workflows. You can do this by using Azure Machine Learning [Python SDK](https://docs.microsoft.com/python/api/overview/azure/ml/?view=azure-ml-py) as follows:

```
from azureml.core import Workspace
from azureml.core.authentication import ServicePrincipalAuthentication

service_principal = ServicePrincipalAuthentication(tenant_id="<YOUR TENANT ID>", 
                                                   service_principal_id="<YOUR CLIENT ID>",
                                                   service_principal_password="<YOUR CLIENT SECRET>") 
workspace = Workspace.get(name="<YOUR WORKSPACE NAME", 
                          auth=service_principal,
                          subscription_id="<YOUR SUBSCRIPTION ID>")
workspace.get_details()
```

### **Authenticate using a managed identity**

You can use managed identity authentication to authenticate from a virtual machine or compute cluster that is configured with a managed identity. Do this by using the Azure Machine Learning [Python SDK](https://docs.microsoft.com/python/api/overview/azure/ml/?view=azure-ml-py), as follows:

```
from azureml.core import Workspace
from azureml.core.authentication import MsiAuthentication

msi_auth = MsiAuthentication()
workspace = Workspace(subscription_id="<YOUR_SUBSCRIPTION_ID",
                      resource_group="<YOUR_RESOURCE_GROUP>",
                      workspace_name="<YOUR_WORKSPACE_NAME",
                      auth=msi_auth)
workspace.get_details()
```

## **Recommended Documents**

* [Set up authentication for Azure Machine Learning resources and workflows](https://docs.microsoft.com/azure/machine-learning/how-to-setup-authentication)
* [Azure Machine Learning SDK documentation](https://docs.microsoft.com/python/api/overview/azure/ml/?view=azure-ml-py)
