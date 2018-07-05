<properties 
	pageTitle="How can I rename a queue/topic after I create it?" 
	description="How can I rename a queue/topic after I create it?" 
	service="microsoft.servicebus"
	resource="namespaces"
	authors="jtaubensee"
	displayOrder="3"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""	
	productPesIds="13186"
	cloudEnvironments="public,BlackForest,Fairfax, MoonCake" 
/>

# How can I rename a queue/topic after I create it?

## **Recommended steps**
* It is not possible to change the name of a queue in the portal, however, you can do so by using the NamespaceManager API and using the RenameQueue method. Please note this only applies to customers on basic and standard messaging plans.

## **Recommended documents**
[More information on the NamespaceManager Class and managing entities](https://msdn.microsoft.com/library/azure/microsoft.servicebus.namespacemanager.aspx)