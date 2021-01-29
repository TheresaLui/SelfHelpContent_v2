<properties
	pageTitle="Server Trust Group issues with Managed Instance"
	description="Server Trust Group issues with Managed Instance"
	infoBubbleText="Server Trust Group issues with Managed Instance"
	service="microsoft.sql"
	resource="servers"
	authors="vtpombei"
	ms.author="vtpombei"
	displayOrder=""
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32749584"
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	articleId="sqlmi-security-srv-trust-group.md"
	ownershipId="AzureData_AzureSQLMI"
/>

# Resolve Server Trust Group issues with Managed Instance

Server trust groups are used to easily manage trust between the set of Azure SQL Managed Instances. This feature is in **preview mode** and currently Server Trust Group can contain only two instances.

## **Recommended Steps**

If you are experiencing some issues with Server Trust Groups, the following steps can help you find a way to troubleshoot the issues:

- It is required that Azure SQL Managed Instances are under the same Azure subscription
- If instances are on different VNets it is required that ports 5024, 11000 - 12000 are allowed

## **Recommended Documents**

* [Server Trust Groups overview](https://docs.microsoft.com/azure/azure-sql/managed-instance/server-trust-group-overview)
