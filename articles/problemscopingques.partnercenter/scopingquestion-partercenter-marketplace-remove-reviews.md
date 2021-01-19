<properties
       pageTitle="Remove reviews from Marketplace store"
       description="Remove reviews from Marketplace store ticketing intake form"
       authors="a-coflor"
       ms.author="a-coflor"
       selfHelpType="problemScopingQuestions"
       supportTopicIds="32785490"
       productPesIds="17006"
       cloudEnvironments="public, fairfax, blackforest, mooncake, ussec, usnat"
       schemaVersion="1"
       articleId="problemscopingques_partnercenter_remove_reviews" 
       clientIds="partnercenter"
	ownershipId="PartnerCenter_Ingestion"
/>
# Remove reviews from Marketplace store

---
{
   "$schema": "SelfHelpContent",
   "resourceRequired": true,
   "subscriptionRequired": true,
   "title": "Remove reviews from Marketplace store",
   "fileAttachmentHint": "Upload any supporting files that can help us understand your issue.",
   "formElements": [
       {
	   "id": "pc_isv_offer_type",
	   "order": 1,
	   "controlType": "dropdown",
	   "displayLabel": "Offer type",
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
	   "id": "business_just",
	   "order": 2,
	   "controlType": "multilinetextbox",
	   "displayLabel": "Business justification",
	   "watermarkText": "Removing a review from Marketplace store fronts requires a business justification",
	   "required": true,
       },
       {
	   "id": "pc_isv_publisher_name",
	   "order": 3,
	   "controlType": "textbox",
	   "displayLabel": "Publisher name",
	   "watermarkText": "Please provide the Publisher name",
	   "required": false
       },
       {
	   "id": "pc_isv_publisher_id",
	   "order": 4,
	   "controlType": "textbox",
	   "displayLabel": "Publisher ID",
	   "watermarkText": "Please provide the Publisher ID",
	   "infoBalloonText": "Open another Partner Center tab and follow these instructions: Select the cog wheel icon on the top right, then Account Settings. Under Organization Profile select Identifiers, the Seller ID & Publisher ID are listed under the Commercial Marketplace section.",
	   "required": false
       },
       {
	   "id": "pc_isv_seller_id",
	   "order": 5,
	   "controlType": "textbox",
	   "displayLabel": "Seller ID",
	   "watermarkText": "Please provide the Seller ID",
	   "infoBalloonText": "Open another Partner Center tab and follow these instructions: Select the cog wheel icon on the top right, then Account Settings. Under Organization Profile select Identifiers, the Seller ID & Publisher ID are listed under the Commercial Marketplace section.",
	   "required": true
       },
       {
	   "id": "problem_description",
	   "order": 6,
	   "controlType": "multilinetextbox",
	   "displayLabel": "Details",
	   "watermarkText": "Please provide any other additional information about your issue",
	   "required": true,
	   "useAsAdditionalDetails": true
       },
       {
	   "id": "problem_start_time",
	   "order": 7,
	   "controlType": "datetimepicker",
	   "displayLabel": "Start Date",
	   "watermarkText": "When did your issue begin?",
	   "required": true
       }
   ]
}
---
