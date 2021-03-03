<properties
	pageTitle="Diagnose and resolve security issues"
	description="Diagnose and resolve security issues"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32677718"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="5bc897a5-e5e8-4e3a-8380-a9b717dd7117"
	ownershipId="AzureData_AzureDatabricks"
/>

# Diagnose and resolve security issues

Most customers can diagnose and resolve security issues using the following steps.

* By default, all users can create and modify workspace objects—including folders, notebooks, experiments, and models—unless an administrator enables workspace access control. With workspace object access control, individual permissions determine a user’s abilities. [This article describes the individual permissions and how to configure workspace object access control](https://docs.microsoft.com/azure/databricks/security/access-control/workspace-acl).

* Enable **[Secure Cluster Connectivity](https://docs.microsoft.com/azure/databricks/security/secure-cluster-connectivity)**, so that customer virtual networks have no open ports and Databricks Runtime cluster nodes have no public IP addresses.

* Sometimes accessing data requires that you authenticate to external data sources through JDBC. Instead of directly entering your credentials into a notebook, use **[Azure Databricks secrets](https://docs.microsoft.com/azure/databricks/security/secrets/)** to store your credentials and reference them in notebooks and jobs. To manage secrets, you can use the Databricks CLI to access the Secrets API. To set up secrets you:
     - [Create a secret scope](https://docs.microsoft.com/azure/databricks/security/secrets/secret-scopes)
     - [Add secrets to the scope](https://docs.microsoft.com/azure/databricks/security/secrets/secrets)
     - If you have the [Azure Databricks Premium Plan](https://databricks.com/product/azure-pricing), assign access control to the secret scope.

* The **'Invalid access token'** error when accessing APIs through Databricks CLI is caused by improper authentication setup for CLI. To resolve the issue, modify the CLI authentication setup using a valid personal access token and then run the CLI commands again. 
	* [Set up Databricks CLI authentication](https://docs.microsoft.com/azure/databricks/dev-tools/cli/?toc=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fazure%2Fazure-databricks%2Ftoc.json&bc=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fazure%2Fbread%2Ftoc.json#--set-up-authentication)
	* [CLI Commands](https://docs.microsoft.com/azure/databricks/dev-tools/cli/?toc=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fazure%2Fazure-databricks%2Ftoc.json&bc=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fazure%2Fbread%2Ftoc.json#cli-commands)
	* [Generate a Personal Access Token](https://docs.microsoft.com/azure/databricks/dev-tools/api/latest/authentication?toc=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fazure%2Fazure-databricks%2Ftoc.json&bc=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fazure%2Fbread%2Ftoc.json#--generate-a-personal-access-token)
	
* Unable to fetch Azure Active Directory access token, and getting the following error:<br>
"{'error':'invalid_resource','error_description':'AADSTS500011: The resource principal named xxx was not found in the tenant named xxx. This can happen if the application has not been installed by the administrator of the tenant or consented to by any user in the tenant. You might have sent your authentication request to the wrong tenant."
	
	This usually occurs when using the incorrect resource authority in the CURL request. To resolve the issue, update `RESOURCE` to the resource management API URI as below:
	
	```$ curl -X POST -d 'grant_type=client_credentials&client_id=[APP_ID]&client_secret=[PASSWORD]&resource=https%3A%2F%2Fmanagement.azure.com%2F' https://login.microsoftonline.com/[TENANT_ID]/oauth2/token```
	
	The response object will contain the `ACCESS_TOKEN`. For more details: [Get an Azure Active Directory access token](https://docs.microsoft.com/azure/databricks/dev-tools/api/latest/aad/service-prin-aad-token#--get-an-azure-active-directory-access-token), [Using cURL and Azure REST API to access Azure Resource Manager](https://gist.github.com/richardjortega/0cc2f1108bccf60f38ea249366886c25#using-curl-and-azure-rest-api-to-access-azure-resource-manager--non-interactive), [Service to service access token request](https://docs.microsoft.com/azure/active-directory/azuread-dev/v1-oauth2-client-creds-grant-flow#request-an-access-token)

## **Recommended Documents**

* [Security and Permissions](https://docs.microsoft.com/azure/databricks/kb/security/)
