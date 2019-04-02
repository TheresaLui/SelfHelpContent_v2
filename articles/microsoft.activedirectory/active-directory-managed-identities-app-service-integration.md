<properties
	pageTitle="User assigned managed identity with Web resources"
	description="I can't add a user-assigned managed identity to my App Service/Function"
	infoBubbleText="An issue was found with a user assigned managed identity on App Service/Function"
	service="microsoft.managedidentity"
	resource="userassignedidentities"
	authors="arluca"
	ms.author="arluca"
	displayOrder=""
	articleId="user-assigned managed identity integration with App Service/Function"
	diagnosticScenario=""
	selfHelpType="resource"
	supportTopicIds="32632154"
	resourceTags=""
	productPesIds="16575"
	cloudEnvironments="public, blackForest, fairfax, mooncake"
/>

# <-- I can't add a user-assigned managed identity to a App Service/Function. -->

For issues related to adding a user-assigned managed identity to an App Service or Azure Function:

## **Recommended Steps**

1. Verify you have the Managed Identity Operator role assignment on the user-assigned managed identity.
2. Verify you have the Contributor role assignment on the App Service/Function.

## **Recommended Documents**

* [How to configure a user-assigned managed identity on an App Service or Azure Function](https://docs.microsoft.com/azure/app-service/overview-managed-identity?context=azure/active-directory/managed-identities-azure-resources/context/msi-context#adding-a-user-assigned-identity-preview)