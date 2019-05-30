<properties
	pageTitle="Azure Migrate Projects (Preview)"
	description="Troubleshooting Azure Migrate Projects (Preview)"
	service="microsoft.migrate"
	resource="projects"
	authors="shijojoy"
	ms.author="shijoy"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32631905"
	resourceTags=""
	productPesIds="16348"
	cloudEnvironments="public"
	articleId="5ba2cff9-3754-4339-ab0f-ee3b617a61a6"
/>

# Troubleshooting Azure Migrate Projects (Preview)

## **Recommended Steps**

* **Error**: The resource type could not be found in the namespace 'microsoft.migrate' for a version '2018-09-01-preview'

This error appears while attempting to create a Resource Group. It can happen if the subscription is not whitelisted for Azure Migrate preview access. To resolve, ask the customer to [sign up](http://aka.ms/migratefuture) to have their subscription ID whitelisted.

* Unable to access Azure Migrate projects in the preview version

1. Go to http://aka.ms/migrate/preview (note that the preview version is only available in this portal and not the regular Azure portal). You can use the regular Azure portal to access the generally available Azure Migrate projects.
2. To access the preview projects, you need to search for "Azure Migrate" in the top search bar then go to “Servers” tab in Azure Migrate to see your machines and assessments. 

