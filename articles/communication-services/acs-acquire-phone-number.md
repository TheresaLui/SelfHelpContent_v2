<properties
	pageTitle="Cannot acquire a phone number"
	description="Cannot acquire a phone number"
	infoBubbleText="Cannot acquire a phone number"
	service="Microsoft.Communication"
	resource="SMS, Calling, Development and Authentication"
	ownershipId="AzureCommunicationServices"
	authors="AriZavala2"
	ms.author="arzavala"
	articleId="acs-acquire-phone-number"
	selfHelpType="diagnostics"
	cloudEnvironments="Public, fairfax, usnat, ussec"
	diagnosticScenario="acs-acquire-phone-number"
/>

# <-- Cannot acquire a phone number -->

<!--issueDescription-->
Customers are getting an error when trying to acquire a phone number. There are a few reasons of why a user cannot acquire a phone number.
<!--/issueDescription-->

## **Recommended Steps**

Sometimes the stock of phone numbers available to purchase runs out. In this case, the phone number type (that is, Geographic or Toll-free) will be dimmed. 
  If this is the case, check back again after some time has passed.

If the failure occurred because of subscription eligibility:<br>
- Check the subscription type. The subscription must be a paid account; the subscription cannot have any free credits associated with it (for example, student accounts, visual studio credits, etc.).
- Check that the billing address is located within the United States, excluding Puerto Rico. Canada and Puerto Rico will be available when the service moves to General Availability.

If this didn't solve the issue, tell the customer to:<br>
- Check our [roadmap](https://github.com/Azure/Communication/projects/1) for future region availability 
- File a [Github issue](https://github.com/Azure/Communication/issues)  for feedback or feature requests 

You can view public documentation on what is currently supported [here](https://docs.microsoft.com/azure/communication-services/concepts/telephony-sms/plan-solution).
