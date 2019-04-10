<properties
	pageTitle="Integration Runtime Express Setup Issue"
	description="Cannot Run Express Setup for Self-hosted IR"
	infoBubbleText=""
	authors="chez-charlie"
	ms.author="chez"
	articleId="e8457178-4061-4b46-b49d-dbdfba49afc4"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32629536"
	resourceTags=""
	productPesIds="15613"
	cloudEnvironments="public"
/>

# Integration Runtime Express Setup Issue

## **Recommended steps**

The Express setup for the Integration Runtime requires Edge or another Microsoft ClickOnce compatible web browser. If the Express Setup fails to start, please consider the following steps:

- Please use Edge or a Microsoft ClickOnce compatible web browser.

  If you are using Chrome, go to the [Chrome web store](https://chrome.google.com/webstore/), search with "ClickOnce" keyword, choose one of the ClickOnce extensions, and install it.

- Use the **Manual Setup** link shown on the same pane in the UI to download the installation file and run it manually. After the installation is successful, you will see the Integration Runtime Configuration dialog box. Copy the **key** from the portal screen and use it in the configuration manager to manually register the gateway with the service.

## **Recommended documents**

[Create and configure Self-hosted Integration Runtime](https://docs.microsoft.com/azure/data-factory/create-self-hosted-integration-runtime/)
