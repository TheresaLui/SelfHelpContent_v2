<properties 
	pageTitle="Why can't I view my namespace in the portal?" 
	description="Why can't I view my namespace in the portal?" 
	service="microsoft.relay"
	resource="namespaces"
	authors="jtaubensee"
	displayOrder="3"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""	
	productPesIds="16123"
	cloudEnvironments="public" 
/>

# I created a Relay namespace before the service was WCF Relay and now I can’t view my namespace here in the portal, but I can see it in the classic portal, why can’t I see it here?

## **Recommended steps**
* We recently separated namespaces to be of a type that is specific to our services. This means that if you created a namespace in the classic portal that is of the namespace type messaging or Event Hub, but contains a relay entity in the namespace it will not be displayed in this portal. In order to see relays in the new portal they need to be of the namespace type Relay. For more information, please read this [blog](https://blogs.msdn.microsoft.com/servicebus/2016/09/14/azure-service-bus-messaging-relay-and-event-hubs-namespace-separation/). We highly recommend any new namespaces created for Relays are of the type Relay when using ARM or you create them in this portal as this is how they will automatically be created.

## **Recommended documents**
[Frequently Asked Questions](https://azure.microsoft.com/documentation/articles/service-bus-relay/relay-faq)<br>
[Common Relay Exceptions](https://azure.microsoft.com/documentation/articles/service-bus-relay/relay-exceptions)