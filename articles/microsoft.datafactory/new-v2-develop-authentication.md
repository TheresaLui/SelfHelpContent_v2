<properties
	pageTitle="Data Factory V2 - Author and Develop - Authentication Failure"
	description="Permissions and Azure Roles for Azure Data Factory"
	infoBubbleText=""
	service="microsoft.datafactory"
	resource="factories"
	authors="chez-charlie"
	ms.author="chez"
	displayOrder="2"
	articleId="b71ce604-505b-45a2-991b-b9fc4596c7d8"
	diagnosticScenario=""
	selfHelpType="resource"
	supportTopicIds="32629441, 32629535"
	resourceTags=""
	productPesIds="15613"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_DataFactory"
/>

# Permissions and Azure Roles for Data Factory

## **Recommended Steps**

- For access control and security purposes, Azure Data Factory requires users to have certain permissions to perform certain tasks
- Please refer to [Azure roles](https://docs.microsoft.com/azure/data-factory/quickstart-create-data-factory-portal#prerequisites) section for high level explanation <br>
- For detailed explanation, please refer to [Roles and permissions for Azure Data Factory](https://docs.microsoft.com/azure/data-factory/concepts-roles-permissions) <br>
- We recommend you consider the built-in [Data Factory Contributor role](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#data-factory-contributor) for data factory resources <br/>

- **NOTES**: To create and manage child resources for Data Factory - including datasets, linked services, pipelines, triggers, and integration runtimes - the following requirements are applicable:
  - To create and manage child resources in the Azure portal, you must belong to __Data Factory Contributor__ role at the _resource group_ level or above
  - To create and manage child resources with PowerShell or SDK, __contributor__ role at _resource_ level or above is sufficient
  - To have more granular access control for ADF portal users, please consider create a separate resource group for your data factory

- **Custom Roles**: To create custom role to grant different access levels for different data factory users, please refer to [Custom scenarios and custom roles](https://docs.microsoft.com/en-us/azure/data-factory/concepts-roles-permissions#custom-scenarios-and-custom-roles)

## **Recommended Documents**

- [Azure Roles section](https://docs.microsoft.com/azure/data-factory/quickstart-create-data-factory-portal#prerequisites) for high level explanation
- [Roles and permissions for Azure Data Factory](https://docs.microsoft.com/azure/data-factory/concepts-roles-permissions)
- [Data Factory Contributor role](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#data-factory-contributor)
