<properties 
	pageTitle="Issues with queues" 
	description="Issues with queues" 
	service="microsoft.servicebus"
	resource="messaging"
	authors="jtaubensee"
	displayOrder="2"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""	
	productPesIds=""
	cloudEnvironments="public" 
/>
    
# Issues with queues
## How can I rename a queue after I create it?
It is not possible to change the name of a queue in the portal, however, you can do so by using the NamespaceManager API and using the RenameQueue method. Please note this only applies to customers on basic and standard messaging plans. Additional info on the NamespaceManager Class and managing entities can be found here: <https://msdn.microsoft.com/library/azure/microsoft.servicebus.namespacemanager.aspx>
