<properties 
	pageTitle="How can I rename a queue/topic after I create it?" 
	description="Learn how to change the name of a queue or topic in the portal, using the NamespaceManager API" 
	service="microsoft.servicebus"
	resource="namespaces"
	authors="jtaubensee"
	ms.author="chiragpa"
	displayOrder="3"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""	
	productPesIds="13186"
	cloudEnvironments="public,BlackForest,Fairfax, MoonCake, usnat, ussec" 
	articleId="cdc14e12-4e6f-490a-93db-179b0e08a425"
	ownershipId="AzureMessaging_Common"
/>

# How can I rename a queue/topic after I create it?

## **Recommended Steps**

* It is not possible to change the name of a queue in the portal, however, you can do so by using the NamespaceManager API and using the RenameQueue method. Please note this only applies to customers on basic and standard messaging plans.

## **Recommended Documents**

* [More information on the NamespaceManager Class and managing entities](https://msdn.microsoft.com/library/azure/microsoft.servicebus.namespacemanager.aspx)
