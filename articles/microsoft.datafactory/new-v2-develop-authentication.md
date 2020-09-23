<properties
  pagetitle="Permissions and Azure Roles for Data Factory"
  service="microsoft.datafactory"
  resource="factories"
  ms.author="chez,vimals"
  selfhelptype="Resource"
  supporttopicids="32629441,32629535"
  resourcetags=""
  productpesids="15613"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="b71ce604-505b-45a2-991b-b9fc4596c7d8"
  ownershipid="AzureData_DataFactory" />
# Permissions and Azure Roles for Data Factory

## **Recommended Steps**

* To create and manage child resources for Data Factory - including datasets, linked services, pipelines, triggers, and integration runtimes in the Azure portal you must belong to the [**_Data Factory Contributor_**](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#data-factory-contributor) role at the **Resource Group** level or above. Refer this article for more details: [Roles and requirements](https://docs.microsoft.com/azure/data-factory/concepts-roles-permissions#roles-and-requirements)<br>

* To create and manage child resources with PowerShell or SDK, _contributor_ role at _resource_ level or above is sufficient<br>

* To have more granular access control for ADF portal users, please consider create a separate resource group for your data factory<br>

* **Custom Roles**: To create custom role to grant different access levels for different data factory users, please refer to [Custom scenarios and custom roles](https://docs.microsoft.com/azure/data-factory/concepts-roles-permissions#custom-scenarios-and-custom-roles)<br>



## **Recommended Documents**

- Refer this article to view or add [Roles and Permissions](https://docs.microsoft.com/azure/role-based-access-control/role-assignments-portal) for a user or service principal
- [Azure Roles section](https://docs.microsoft.com/azure/data-factory/quickstart-create-data-factory-portal#prerequisites) for high level explanation
- [Roles and permissions for Azure Data Factory](https://docs.microsoft.com/azure/data-factory/concepts-roles-permissions)
- [Data Factory Contributor role](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#data-factory-contributor)