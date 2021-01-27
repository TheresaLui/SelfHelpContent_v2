<properties
       pageTitle="Marketplace Pricing issue"
       description="Marketplace Pricing issue ticketing intake form"
       authors="A-COFLOR"
       ms.author="A-COFLOR"
       selfHelpType="problemScopingQuestions"
       supportTopicIds="32728249,32728277,32728206,32728186,32728076,32728030"
       productPesIds="17006"
       cloudEnvironments="public, fairfax, blackforest, mooncake, ussec, usnat"
       schemaVersion="1"
       articleId="problemscoping_partnercenter_marketplace_pricing" 
       clientIds="partnercenter"
	ownershipId="PartnerCenter_Ingestion"
/>
# Marketplace Pricing Issues

---
{
   "$schema": "SelfHelpContent",
   "resourceRequired": true,
   "subscriptionRequired": true,
   "title": "Marketplace Pricing Issues",
   "fileAttachmentHint": "Please provide a screen recording (PSR) or document with an updated pricing .xls (required for VM), error message, steps, or screenshots to recreate the issue",
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
	   "displayLabel": "Offer Type:",
       "watermarkText":"Please select the Offer Type from the below list",
	   "dropdownOptions": [
	       {
		   "value": "consulting_service_offer",
		   "text": "Consulting Service offer"
	       },
	       {
		   "value": "office_add",
		   "text": "Office add-in"
	       },
	       {
		   "value": "power_bi_visual",
		   "text": "Power BI visual"
	       },
	       {
		   "value": "sharepoint_add",
		   "text": "SharePoint add-in"
	       },
	       {
		   "value": "azure_vm_offer",
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
