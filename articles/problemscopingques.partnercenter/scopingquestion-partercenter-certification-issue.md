<properties
       pageTitle="Marketplace Certification issue"
       description="Marketplace Certification issue ticketing intake form"
       authors="A-COFLOR"
       ms.author="A-COFLOR"
       selfHelpType="problemScopingQuestions"
       supportTopicIds="32728246,32728013,32728159,32728086,32728203,32728125,32728217,32728260,32728112,32728166,32728183,32728099,32728274,32728072,32728233,32728052"
       productPesIds="17009"
       cloudEnvironments="public, fairfax, blackforest, mooncake, ussec, usnat"
       schemaVersion="1"
       articleId="problemscopingques_partnercenter_certification_issue"
       clientIds="partnercenter"
	ownershipId="PartnerCenter_Offer_Certification"
/>
# Certification issue

---
{
   "$schema": "SelfHelpContent",
   "resourceRequired": true,
   "subscriptionRequired": true,
   "title": "Marketplace Certification Issue",
   "fileAttachmentHint": "Please upload any supporting files that can help us better understand your issue (screen recording or a document with steps to recreate the issue)",
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
	   "id": "pc_isv_offer_type",
	   "order": 4,
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
	   "id": "business_justification",
	   "order": 8,
	   "controlType": "multilinetextbox",
	   "displayLabel": "Business justification",
	   "watermarkText": "Expediting the certification process is not supported unless there is a strong business justification",
	   "required": false
       },
       {
	   "id": "problem_description",
	   "order": 9,
	   "controlType": "multilinetextbox",
	   "displayLabel": "Details",
	   "watermarkText": "Please provide any other additional information about your issue",
	   "required": true,
	   "useAsAdditionalDetails": true
       },
       {
	   "id": "problem_start_time",
	   "order": 10,
	   "controlType": "datetimepicker",
	   "displayLabel": "Start Date",
	   "watermarkText": "When did your issue begin?",
	   "required": true
       }
   ]
}
---
