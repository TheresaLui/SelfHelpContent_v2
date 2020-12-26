<properties
  pagetitle="Permissions and Azure Roles for Data Factory&#xD;"
  service="microsoft.datafactory"
  resource="factories"
  ms.author="chez,vimals,haoc"
  selfhelptype="Resource"
  supporttopicids="32629441,32629535"
  resourcetags=""
  productpesids="15613"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="b71ce604-505b-45a2-991b-b9fc4596c7d8"
  ownershipid="AzureData_DataFactory" />
# Permissions and Azure Roles for Data Factory

## **Recommended Steps**

* To create and manage child resources for Data Factory, including datasets, linked services, pipelines, triggers, and integration runtimes in the Azure portal, you must have the [**Data Factory Contributor**](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#data-factory-contributor) role at the **Resource Group** level or above. For more information, see [Roles and requirements](https://docs.microsoft.com/azure/data-factory/concepts-roles-permissions#roles-and-requirements).<br>

* To create and manage child resources with PowerShell or SDK, the **Data Factory Contributor** role at the Resource level or above is sufficient<br>

* To have more granular access control for ADF portal users, consider creating a separate resource group for your data factory<br>

* **Custom roles**: To create custom role to grant different access levels for different data factory users, see [Custom scenarios and custom roles](https://docs.microsoft.com/azure/data-factory/concepts-roles-permissions#custom-scenarios-and-custom-roles)<br>

* If you've moved Data Factory from one tenant to another, and you're having issues, try generating a new managed identity. You can use Powershell or the REST API. For more information, see [Generate service identity](https://docs.microsoft.com/azure/data-factory/data-factory-service-identity#generate-service-identity).

## **Recommended Documents**

- [Roles and Permissions](https://docs.microsoft.com/azure/role-based-access-control/role-assignments-portal) to view or add roles for a user or service principal
- [Azure Roles section](https://docs.microsoft.com/azure/data-factory/quickstart-create-data-factory-portal#prerequisites)
- [Roles and permissions for Azure Data Factory](https://docs.microsoft.com/azure/data-factory/concepts-roles-permissions)
- [Data Factory Contributor role](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#data-factory-contributor)