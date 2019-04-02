<properties
	pageTitle="Azure Migrate preview - Creating a migration project"
	description="Azure Migrate preview - Creating a migration project"
	service="microsoft.migrate"
	resource="projects"
	authors="shijojoy"
	ms.author="shijoy"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32631922"
	resourceTags=""
	productPesIds="16348"
	cloudEnvironments="public"
	articleId="ecf87d57-c8c4-4009-8d82-f6d50af6c981"
/>

# Azure Migrate preview - Creating a migration project

## **Recommended Steps**

### **Unable to create a Resource Group.'The resource type could not be found in the namespace 'microsoft.migrate' for a version '2018-09-01-preview'**
Root cause: This can happen if the subscription is not whitelisted for Azure Migrate preview access.

Fix: Ask the customer to sign up here to get their subscription ID whitelisted: http://aka.ms/migratefuture

### **Unable to access Azure Migrate projects in the preview version**
	1. Go to http://aka.ms/migrate/preview (Note that the preview version is only available in this portal and not the regular Azure portal). You can use the regular Azure portal (portal.azure.com) to access the generally available Azure Migrate projects.
	2. To access the preview projects, you need to search for ‘Azure Migrate’ in the top search bar and then go to “Servers” tab in Azure Migrate to see your machines and assessments. 
