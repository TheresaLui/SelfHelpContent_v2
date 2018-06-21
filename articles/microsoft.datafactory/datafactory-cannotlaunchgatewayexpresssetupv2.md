<properties 
	pageTitle="I cannot launch Integration Runtime Express Setup" 
	description="I cannot launch Integration Runtime Express Setup." 
	service="microsoft.datafactory" 
    resource="factories"
    authors="arthurw"
    displayOrder="8"
    selfHelpType="resource"
	cloudEnvironments="public" 	
    supportTopicIds="32356656"
    productPesIds="15613"
    resourceTags=""
/>

# I cannot launch Integration Runtime Express Setup

## **Recommended steps**
The Express setup for the Integration Runtime requires Edge or another Microsoft ClickOnce compatible web browser. If the Express Setup fails to start, do one of the following: 

- Please use Edge or a Microsoft ClickOnce compatible web browser.

	If you are using Chrome, go to the [Chrome web store](https://chrome.google.com/webstore/), search with "ClickOnce" keyword, choose one of the ClickOnce extensions, and install it. 

- Use the **Manual Setup** link shown on the same pane in the UI to download the installation file and run it manually. After the installation is successful, you will see the Integration Runtime Configuration dialog box. Copy the **key** from the portal screen and use it in the configuration manager to manually register the gateway with the service. 

## **Recommended documents**
[How to create and configure Self-hosted Integration Runtime](https://docs.microsoft.com/azure/data-factory/create-self-hosted-integration-runtime/)
