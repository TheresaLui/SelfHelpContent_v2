<properties
       pageTitle="Marketplace Payout issue"
       description="Marketplace Payout issue ticketing intake form"
       authors="A-COFLOR"
       ms.author="A-COFLOR"
       selfHelpType="problemScopingQuestions"
       supportTopicIds="32750772,32728043,32750771,32750767,32750766,32750769,32750765,32750775,32750776,32750773,32728069"
       productPesIds="17010"
       cloudEnvironments="public, fairfax, blackforest, mooncake, ussec, usnat"
       schemaVersion="1"
       articleId="problemscopingques_partnercenter_payout_issue"
       clientIds="partnercenter"
	ownershipId="PartnerCenter_Payouts"
/>

# Payout issue
---
{
   "$schema": "SelfHelpContent",
   "resourceRequired": true,
   "subscriptionRequired": true,
   "title": "Marketplace Deployment Issue",
   "fileAttachmentHint": "Please upload any supporting files that can help us better understand your issue (screen recording or a document with steps/screenshots to recreate the issue)",
   "formElements": [
       {
	   "id": "pc_isv_publisher_name",
	   "order": 1,
	   "controlType": "textbox",
	   "displayLabel": "Publisher name",
	   "watermarkText": "Please provide the Publisher name",
	   "required": false
       },
       {
	   "id": "pc_isv_publisher_id",
	   "order": 2,
	   "controlType": "textbox",
	   "displayLabel": "Publisher ID",
	   "watermarkText": "Please provide the Publisher ID",
	   "infoBalloonText": "Open another Partner Center tab and follow these instructions: Select the cog wheel icon on the top right, then Account Settings. Under Organization Profile select Identifiers, the Seller ID & Publisher ID are listed under the Commercial Marketplace section.",
	   "required": false
       },
       {
	   "id": "pc_isv_seller_id",
	   "order": 3,
	   "controlType": "textbox",
	   "displayLabel": "Seller ID",
	   "watermarkText": "Please provide the Seller ID",
	   "infoBalloonText": "Open another Partner Center tab and follow these instructions: Select the cog wheel icon on the top right, then Account Settings. Under Organization Profile select Identifiers, the Seller ID & Publisher ID are listed under the Commercial Marketplace section.",
	   "required": true
       },
       {
	   "id": "pc_isv_transaction_identifier",
	   "order": 4,
	   "controlType": "textbox",
	   "displayLabel": "Transaction Identifier (e.g. PaymentID, earningID, transactionID)",
	   "watermarkText": "Enter the PaymentID, earningID, transactionID or other identifier",
	   "required": false
       },
       {
	   "id": "pc_isv_offer_id",
	   "order": 5,
	   "controlType": "textbox",
	   "displayLabel": "Offer ID",
	   "watermarkText": "Please provide the Offer ID",
	   "required": false
       },
       {
	   "id": "pc_isv_offer_name",
	   "order": 6,
	   "controlType": "textbox",
	   "displayLabel": "Offer Name",
	   "watermarkText": "Please provide the Offer Name",
	   "required": false
       },
       {
	   "id": "pc_isv_offer_type",
	   "order": 7,
	   "controlType": "dropdown",
	   "displayLabel": "Offer Type",
       "watermarkText":"Please select the Offer Type from the below list",
	   "dropdownOptions": [
	       {
		   "value": "Azure Application offer",
		   "text": "Azure Application offer"
	       },
	       {
		   "value": "Consulting Service offer",
		   "text": "Consulting Service offer"
	       },
	       {
		   "value": "Azure Container offer",
		   "text": "Azure Container offer"
	       },
	       {
		   "value": "Dynamics 365 business central offer",
		   "text": "Dynamics 365 business central offer"
	       },
	       {
		   "value": "Dynamics 365 for Customer Engagement & Power Apps offer",
		   "text": "Dynamics 365 for Customer Engagement & Power Apps offer"
	       },
	       {
		   "value": "Dynamics 365 for operations offer",
		   "text": "Dynamics 365 for operations offer"
	       },
	       {
		   "value": "IoT Edge Module Offer",
		   "text": "IoT Edge Module Offer"
	       },
	       {
		   "value": "Managed service offer",
		   "text": "Managed service offer"
	       },
	       {
		   "value": "Office add-in",
		   "text": "Office add-in"
	       },
	       {
		   "value": "Power BI visual",
		   "text": "Power BI visual"
	       },
	       {
		   "value": "PowerBI app offer",
		   "text": "PowerBI app offer"
	       },
	       {
		   "value": "Software as a Service offer",
		   "text": "Software as a Service offer"
	       },
	       {
		   "value": "SharePoint add-in",
		   "text": "SharePoint add-in"
	       },
	       {
		   "value": "Teams app product",
		   "text": "Teams app product"
	       },
	       {
		   "value": "Azure Virtual machine offer",
		   "text": "Azure Virtual machine offer"
	       },
	       {
		   "value": "dont_know_answer",
		   "text": "Not sure"
	       }
	       ],
	   "required": true
       },
       {
	   "id": "pc_isv_contact_method",
	   "order": 8,
	   "controlType": "dropdown",
	   "displayLabel": "Preferred contact method",
       "watermarkText":"Please select the preferred contact method from the below list",
	   "dropdownOptions": [
	       {
		   "value": "Preferred method email",
		   "text": "Email"
	       },
	       {
		   "value": "Preferred method phone",
		   "text": "Phone"
	       },
               {
		   "value": "Preferred method Teams",
		   "text": "Teams"
	       }],
	   "required": false
       },
       {
	   "id": "problem_start_time",
	   "order": 10,
	   "controlType": "datetimepicker",
	   "displayLabel": "Start Date",
	   "watermarkText": "When did your issue begin?",
	   "required": true
       },
       {
	   "id": "problem_description",
	   "order": 11,
	   "controlType": "multilinetextbox",
	   "displayLabel": "Details",
	   "watermarkText": "Please provide any other additional information about your issue",
	   "required": true,
	   "useAsAdditionalDetails": true
       }
   ]
}
---
