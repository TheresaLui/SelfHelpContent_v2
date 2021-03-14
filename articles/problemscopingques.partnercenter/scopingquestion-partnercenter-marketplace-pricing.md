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
	   "id": "pc_isv_offer_type",
       "order": 1,
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
	   "order": 2,
	   "controlType": "multilinetextbox",
	   "displayLabel": "Details",
	   "watermarkText": "Please provide any other additional information about your issue",
	   "required": true,
	   "useAsAdditionalDetails": true
       },
       {
	   "id": "problem_start_time",
	   "order": 3,
	   "controlType": "datetimepicker",
	   "displayLabel": "Start Date",
	   "watermarkText": "When did your issue begin?",
	   "required": true
       }
   ]
}
---
