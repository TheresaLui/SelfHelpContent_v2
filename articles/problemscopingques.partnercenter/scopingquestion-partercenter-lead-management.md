<properties
       pageTitle="Marketplace Lead Management"
       description="Marketplace Lead Management issue ticketing intake form"
       authors="A-COFLOR"
       ms.author="A-COFLOR"
       selfHelpType="problemScopingQuestions"
       supportTopicIds="32728033"
       productPesIds="17006"
       cloudEnvironments="public, fairfax, blackforest, mooncake, ussec, usnat"
       schemaVersion="1"
       articleId="problemscopingques_partnercenter_lead_management"
       clientIds="partnercenter"
	ownershipId="PartnerCenter_Ingestion"
/>
# Payout issue

---
{
   "$schema": "SelfHelpContent",
   "resourceRequired": true,
   "subscriptionRequired": true,
   "title": "Marketplace Lead Management Issues",
   "fileAttachmentHint": "Please upload any supporting files that can help us better understand your issue (screen recording or a document with steps to recreate the issue)",
   "formElements": [
       {
	   "id": "pc_isv_publisher_name",
	   "order": 1,
	   "controlType": "textbox",
	   "displayLabel": "Publisher name",
	   "watermarkText": "Please provide the publisher name",
	   "required": flase
       },
       {
	   "id": "pc_isv_publisher_id",
	   "order": 2,
	   "controlType": "textbox",
	   "displayLabel": "Publisher ID",
	   "watermarkText": "In Partner Center select Settings then Developer settings",
	   "required": false
       },
       {
	   "id": "pc_isv_seller_id",
	   "order": 3,
	   "controlType": "textbox",
	   "displayLabel": "Please provide the seller ID",
	   "watermarkText": "In Partner Center select Settings then Developer settings",
	   "required": true
       },
       {
	   "id": "additional_email_for_notification",
	   "order": 4,
	   "controlType": "textbox",
	   "displayLabel": "Additional email(s) for notification",
	   "watermarkText": "Please add name@emailaddress.com here if you'd like us to include others on the SR communications",
	   "required": false
       },
       {
	   "id": "pc_isv_lead_destination",
	   "order": 5,
	   "controlType": "dropdown",
	   "displayLabel": "Lead Destination",
       "watermarkText":"Please select Lead Destination from the below list",
	   "dropdownOptions": [
	       {
		   "value": "dynamics_crm_online",
		   "text": "Dynamics CRM Online"
	       },
	       {
		   "value": "marketo",
		   "text": "Marketo"
	       },
	       {
		   "value": "salesforce",
		   "text": "Salesforce"
	       },
	       {
		   "value": "azure_table",
		   "text": "Azure Table"
	       },
           {
		   "value": "https_endpoint",
		   "text": "HTTPS Endpoint"
	       }],
	   "required": false
       },
       {
	   "id": "pc_isv_offer_type",
	   "order": 6,
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
	   "id": "pc_isv_offer_name",
	   "order": 7,
	   "controlType": "textbox",
	   "displayLabel": "Offer Name",
	   "watermarkText": "Please provide the Offer Name",
	   "required": false
       },
       {
	   "id": "pc_isv_offer_d365",
	   "order": 8,
	   "controlType": "dropdown",
	   "displayLabel": "Is Offer D365 type?",
       "watermarkText":"Choose from below",
	   "dropdownOptions": [
	       {
		   "value": "Yes",
		   "text": "Yes"
	       },
           {
		   "value": "No",
		   "text": "No"
	       }],
	   "required": false
       },
       {
	   "id": "pc_isv_d365offer_true",
	   "order": 9,
	   "controlType": "textbox",
	   "displayLabel": "If Offer is D365 type, please provide the Environment Name and Environment Type",
	   "watermarkText": "Environment Name; Environment Type",
	   "required": false
       },
       {
	   "id": "problem_start_time",
	   "order": 10,
	   "controlType": "datetimepicker",
	   "displayLabel": "Start Time",
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
