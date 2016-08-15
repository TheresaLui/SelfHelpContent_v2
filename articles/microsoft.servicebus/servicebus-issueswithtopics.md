<properties 
	pageTitle="Issues with topics" 
	description="Issues with topics" 
	service="microsoft.servicebus"
	resource="messaging"
	authors="jtaubensee"
	displayOrder="3"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""	
	productPesIds=""
	cloudEnvironments="public" 
/>
    
# Issues with topics
## How can I rename a topic after I create it?
It is not possible to change the name of a topic in the portal, however, you can do so by using the NamespaceManager API and using the RenameTopic method. Please note this only applies to customers on basic and standard messaging plans. Additional info on the NamespaceManager Class and managing entities can be found here: <https://msdn.microsoft.com/library/azure/microsoft.servicebus.namespacemanager.aspx>
