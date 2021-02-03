<properties
  pagetitle="Roles and Permissions for Data Factory&#xD;"
  service="microsoft.datafactory"
  resource="factories"
  ms.author="chez,haoc,vimals"
  selfhelptype="Resource"
  supporttopicids="32629535"
  resourcetags=""
  productpesids="15613"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="b71ce604-505b-45a2-991b-b9fc4596c7d8"
  ownershipid="AzureData_DataFactory" />
# Roles and Permissions for Data Factory

Use the following guidelines to assign permissions and roles in Azure Data Factory (ADF).

## **Recommended Steps**

* To create and manage child resources for Azure Data Factory (including datasets, linked services, pipelines, triggers, and integration runtimes in the Azure portal), you must have the **Data Factory Contributor** role at the **Resource Group** level or above. For more information, see [Roles and requirements](https://docs.microsoft.com/azure/data-factory/concepts-roles-permissions#roles-and-requirements).<br>

* To create and manage child resources with PowerShell or SDK, you'll need the **Data Factory Contributor** role at the Resource Group level or above<br>

* To have greater access control for ADF portal users, consider creating a separate resource group for your data factory<br>

* To grant different access levels to different data factory users, create a **Custom** role. See [Custom scenarios and custom roles](https://docs.microsoft.com/azure/data-factory/concepts-roles-permissions#custom-scenarios-and-custom-roles).<br>

* If you moved Data Factory from one tenant to another and are having issues, try generating a new managed identity. To do this, you can use PowerShell or the REST API. For more information, see [Generate service identity](https://docs.microsoft.com/azure/data-factory/data-factory-service-identity#generate-service-identity).

## **Recommended Documents**

- [Roles and Permissions](https://docs.microsoft.com/azure/role-based-access-control/role-assignments-portal) to view or add roles for a user or service principal
- [Azure Roles section](https://docs.microsoft.com/azure/data-factory/quickstart-create-data-factory-portal#prerequisites)
- [Roles and permissions for Azure Data Factory](https://docs.microsoft.com/azure/data-factory/concepts-roles-permissions)
- [Data Factory Contributor role](https://docs.microsoft.com/azure/role-based-access-control/built-in-roles#data-factory-contributor)
