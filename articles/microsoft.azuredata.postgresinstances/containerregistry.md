<properties
  pagetitle="Microsoft Container Registry (MCR) for PostgreSQL Hyperscale Azure Arc"
  service="microsoft.azuredata"
  resource="postgresinstances"
  ms.author="pookam"
  selfhelptype="Generic"
  supporttopicids="32747905"
  productpesids="17124"
  cloudEnvironments="public, fairfax, usnat, ussec"
  articleid="b559f659-653f-493a-8869-7ec018f30ed2"
  ownershipid="AzureData_Azure_Arc_enabled_PostgreSQL_Hyperscale" />
    
# Microsoft Container Registry (MCR) for PostgreSQL Hyperscale Azure Arc.

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
   $ kubectl describe pod podname
   ```

   Sample result:

   ```bash
   mssql-miaa:
        ...
	    Container ID:   docker://d04bcbcb8c6522a925b57c561a7bbf55d005f5f673af18c23f8bad06b015914b
	    Image:          azurearcdata.azurecr.io/azure-arc-data/mssql-miaa:private-preview-jul-2020-new
	    Image ID:       docker-pullable://azurearcdata.azurecr.io/azure-arc-data/"
   ```