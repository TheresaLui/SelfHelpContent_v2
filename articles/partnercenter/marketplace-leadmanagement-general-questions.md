<properties
	pageTitle="Lead Management for Commercial Marketplace"
	description="Frequently asked questions and issues for lead management"
	infoBubbleText=""
	service="partnercenter"
	resource="marketplace"
	authors="keferna"
	ms.author="keferna"
	displayOrder=""
	articleId="marketplace_leadmanagement_faq"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32728033"
    clientIds="partnercenter"
	resourceTags="marketplace"
	productPesIds="17006"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="PartnerCenter_Ingestion"
/>

# Commercial marketplace - Lead management configuration

FAQs and resources for lead management configuration for offers in the commercial marketplace.



## **Recommended Steps**

1. Select a lead destination where you want us to send customer leads. The following CRM systems are supported:
* [Dynamics 365 for Customer Engagement](https://docs.microsoft.com/azure/marketplace/partner-center-portal/commercial-marketplace-lead-management-instructions-dynamics) 
* [Salesforce](https://docs.microsoft.com/azure/marketplace/partner-center-portal/commercial-marketplace-lead-management-instructions-salesforce) 
* [Marketo CRM](https://docs.microsoft.com/azure/marketplace/partner-center-portal/commercial-marketplace-lead-management-instructions-marketo) 
* If your CRM system is not explicitly supported in the list above, you have the following options that allow you to store the customer lead data, and then you can export or import this data into your CRM system.
	* [Azure table](https://docs.microsoft.com/azure/marketplace/partner-center-portal/commercial-marketplace-lead-management-instructions-azure-table) 
	* [Microsoft Flow with a https endpoint](https://docs.microsoft.com/azure/marketplace/partner-center-portal/commercial-marketplace-lead-management-instructions-https) 

2. Read the documentation linked above to your selected lead destination to see how to set up the lead destination to receive leads from your marketplace offer. Proceed to step 3 after you have successfully completed step 2.
3. Connect your offer to the lead destination while publishing the offer to the marketplace in Partner Center. See the documentation linked in step 1 for how to do this.
4. Confirm the connection to the lead destination is set up properly. You can do so by clicking the "Validate" button available in the window where you are configuring the connection to your lead management destination in Partner Center. 
5. After validating the connection to the lead destination is successful, publish the offer in Partner Center. When you are viewing the offer before you go live (preview version of your offer), you can also test your lead connection by trying to acquire the offer yourself in the preview environment.
6. Make sure the connection to the lead destination stays up-to-date so that you don’t lose any leads. Thus, ensure you update these connections in Partner Center whenever something has changed on your CRM.

**Frequently asked questions**



**I am having issues connecting my offer to my Dynamics 365 CRM system.**
* Make sure you have followed all the instructions documented [here](https://docs.microsoft.com/azure/marketplace/partner-center-portal/commercial-marketplace-lead-management-instructions-dynamics)
* Make sure you have the lead writer solution successfully installed in your Dynamics CRM system. You may need your CRM admin's help.
* Make sure the lead writer solution has been granted the right permissions in your Dynamics CRM system
* If you are using Office 365 for authentication, verify that the password is not expired. Also, make sure that multi-factor authentication is not required.
* Make sure you re-publish the offer in Partner Center to make any lead configuration changes take effect. The configuration changes will not take effect until you re-publish the offer.

If you have followed all the above steps and are still having trouble:
* Re-download the [lead writer solution](https://mpsapiprodwus.blob.core.windows.net/documentation/MicrosoftMarketplacesLeadIntegrationSolution_1_0_0_0_target_CRM_6.1_managed.zip) and re-install it in your Dynamics CRM.
* Contact your Dynamics CRM admin or Dynamics support team for help. Sometimes when the Dynamics CRM system has special configurations, the lead writer solution is not able to send leads to the system.
* Choose a different way to receive leads. You can create an Azure table to store leads and then export the data to your CRM system or you can use Microsoft Flow to send an email when a lead is generated.

**My CRM system is not explicitly supported. How do I get leads?**

You can create an Azure table to store leads and then export the data to your CRM system or you can use Microsoft Flow to send an email when a lead is generated.



**I have received an email that a customer is interested in my offer but I don't have their contact information.**

The customer's contact information can be found in the lead destination configured for the offer (Dynamics, Salesforce, Azure table, etc.). If you don't know the configured lead destination, reach out to someone in your company that may know.



**I am not able to filter marketplace leads based on my CRM's country codes.**

Country field values for marketplace leads are open ended and are not provided via country codes. The customer can provide any value for this field. Please look at other ways to achieve your desired outcome.



**How do I know if the connection to my lead destination is correct?**

You have the option to validate your connection while setting up the configuration in Partner Center. Click the "validate" button and you will see if the connection is correct.



## **Recommended Documents**

* [Lead Management Overview](https://docs.microsoft.com/azure/marketplace/partner-center-portal/commercial-marketplace-get-customer-leads)
* [Other frequently asked questions](https://docs.microsoft.com/azure/marketplace/partner-center-portal/commercial-marketplace-get-customer-leads#leads-frequently-asked-questions)
* [Instructions for Dynamics 365 for Customer Engagement](https://docs.microsoft.com/azure/marketplace/partner-center-portal/commercial-marketplace-lead-management-instructions-dynamics)
* [Instructions for Marketo CRM](https://docs.microsoft.com/azure/marketplace/partner-center-portal/commercial-marketplace-lead-management-instructions-marketo)
* [Instructions for Salesforce CRM](https://docs.microsoft.com/azure/marketplace/partner-center-portal/commercial-marketplace-lead-management-instructions-salesforce)
* [Instructions for Azure table to store lead info](https://docs.microsoft.com/azure/marketplace/partner-center-portal/commercial-marketplace-lead-management-instructions-azure-table)
* [Instructions for Microsoft Flow using an HTTPS endpoint to send an email when a lead is generated](https://docs.microsoft.com/azure/marketplace/partner-center-portal/commercial-marketplace-lead-management-instructions-https)
