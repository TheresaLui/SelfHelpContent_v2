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

* Enable **[Secure Cluster Connectivity](https://docs.microsoft.com/azure/databricks/security/secure-cluster-connectivity)**, so that customer virtual networks have no open ports and Databricks Runtime cluster nodes have no public IP addresses.

* Facing **'Invalid access token'** error when accessing APIs through Databricks CLI, this is due to improper authentication setup for CLI. To resolve the issue, please modify the CLI authentication setup using a valid personal access token and then try to run the CLI commands again. 
	* [Set up Databricks CLI authentication](https://docs.microsoft.com/azure/databricks/dev-tools/cli/?toc=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fazure%2Fazure-databricks%2Ftoc.json&bc=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fazure%2Fbread%2Ftoc.json#--set-up-authentication)
	* [CLI Commands](https://docs.microsoft.com/azure/databricks/dev-tools/cli/?toc=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fazure%2Fazure-databricks%2Ftoc.json&bc=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fazure%2Fbread%2Ftoc.json#cli-commands)
	* [Generate a Personal Access Token](https://docs.microsoft.com/azure/databricks/dev-tools/api/latest/authentication?toc=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fazure%2Fazure-databricks%2Ftoc.json&bc=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fazure%2Fbread%2Ftoc.json#--generate-a-personal-access-token)
	
* Unable to fetch Azure Active Directory access token getting error:
	
	``` {'error':'invalid_resource','error_description':'AADSTS500011: The resource principal named xxx was not found in the tenant named xxx. This can happen if the application has not been installed by the administrator of the tenant or consented to by any user in the tenant. You might have sent your authentication request to the wrong tenant.```
	
	This usually occurs when using incorrect resource authority in the CURL request. To resolve the issue, please update RESOURCE to the resource management API URI as below:
	
	```$ curl -X POST -d 'grant_type=client_credentials&client_id=[APP_ID]&client_secret=[PASSWORD]&resource=https%3A%2F%2Fmanagement.azure.com%2F' https://login.microsoftonline.com/[TENANT_ID]/oauth2/token```
	
	The response object will contain the ACCESS_TOKEN. For more details: [Get an Azure Active Directory access token](https://docs.microsoft.com/azure/databricks/dev-tools/api/latest/aad/service-prin-aad-token#--get-an-azure-active-directory-access-token), [Using cURL and Azure REST API to access Azure Resource Manager](https://gist.github.com/richardjortega/0cc2f1108bccf60f38ea249366886c25#using-curl-and-azure-rest-api-to-access-azure-resource-manager--non-interactive), [Service to service access token request](https://docs.microsoft.com/azure/active-directory/azuread-dev/v1-oauth2-client-creds-grant-flow#request-an-access-token)

## **Recommended Documents**

* [Security and Permissions](https://docs.microsoft.com/azure/databricks/kb/security/)
