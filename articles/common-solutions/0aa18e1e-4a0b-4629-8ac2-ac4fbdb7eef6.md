<properties
  pagetitle="Microsoft Container Registry (MCR) for SQL Managed Instance Azure Arc."
  service="microsoft.azuredata"
  resource="sqlmanagedinstances"
  ms.author="jopilov"
  selfhelptype="Generic"
  supporttopicids="32743983"
  resourcetags=""
  productpesids="17125"
  cloudEnvironments="public, fairfax, usnat, ussec"
  articleid="0aa18e1e-4a0b-4629-8ac2-ac4fbdb7eef6"
  ownershipid="AzureData_Managed_Instance_Azure_Arc" />
# Microsoft Container Registry (MCR) for SQL Managed Instance Azure Arc.

Most users are able to resolve their container registry related to registration and deployment of an Azure Arc Managed Instance.

## **Recommended Steps**

1. You can list the container registry from which the Arc Data Controller is configured to pull images. By default it is Microsoft Container Registry (MCR):

   ```bash
   azdata arc dc config show |grep registry
   ```
   Sample Result:

   ```
   "dockerRegistry": "mssql-private-registry",
   "registry": "azurearcdata.azurecr.io",
   ```

1. You can also list which registry the currently-running image was pulled from by looking at the Image ID in the pod description:

   ```bash
   $ kubectl get pods
   $ kubectl describe pod sqlmi1-0
   ```

   Sample result:

   ```bash
   mssql-miaa:
        ...
	    Container ID:   docker://d04bcbcb8c6522a925b57c561a7bbf55d005f5f673af18c23f8bad06b015914b
	    Image:          azurearcdata.azurecr.io/azure-arc-data/mssql-miaa:private-preview-jul-2020-new
	    Image ID:       docker-pullable://azurearcdata.azurecr.io/azure-arc-data/"
   ```