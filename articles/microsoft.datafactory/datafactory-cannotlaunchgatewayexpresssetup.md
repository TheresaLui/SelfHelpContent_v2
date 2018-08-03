<properties 
	pageTitle="I cannot launch Integration Runtime (Data Management Gateway) Express Setup" 
	description="I cannot launch Integration Runtime (Data Management Gateway) Express Setup." 
	service="microsoft.datafactory" 
    resource="datafactories"
    authors="spelluru"
    displayOrder="3"
    selfHelpType="resource"
	cloudEnvironments="public" 	
    supportTopicIds="32356656"
    productPesIds="15613"
    resourceTags=""
/>

# I cannot launch Integration Runtime (Data Management Gateway) Express Setup

## **Recommended steps**
The Express setup for the self-hosted Integration Runtime (formerly called Data Management Gateway) requires Edge, Internet Explorer, or another Microsoft ClickOnce compatible web browser. If the Express Setup fails to start, do one of the following: 

- Please use Edge, Internet Explorer, or another Microsoft ClickOnce compatible web browser.

	If you are using Chrome, go to the [Chrome web store](https://chrome.google.com/webstore/), search with "ClickOnce" keyword, choose one of the ClickOnce extensions, and install it. 

	You need to do the same for Firefox (install add-in). Click Open Menu button on the toolbar (three horizontal lines in the top-right corner), click Add-ons, search with "ClickOnce" keyword, choose one of the ClickOnce extensions, and install it. 

- Use the **Manual Setup** link shown on the same blade in the portal to download installation file and run it manually. After the installation is successful, you will see the Integration Runtime Configuration dialog box. Copy the **key** from the portal screen and use it in the configuration manager to manually register the gateway with the service. 

## **Recommended documents**
[Move data between on-premises and cloud with Data Management Gateway](https://docs.microsoft.com/azure/data-factory/v1/data-factory-move-data-between-onprem-and-cloud)
