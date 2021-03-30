<properties
       pageTitle="Marketplace Microsoft 365 App Compliance program issues"
       description="Marketplace Microsoft 365 App Compliance program issues ticketing intake form"
       authors="A-COFLOR"
       ms.author="A-COFLOR"
       selfHelpType="problemScopingQuestions"
       supportTopicIds="32779866,32779867,32779868,32779869"
       productPesIds="17006"
       cloudEnvironments="public, fairfax, blackforest, mooncake, ussec, usnat"
       schemaVersion="1"
       articleId="problemscoping_partnercenter_marketplace_m365" 
       clientIds="partnercenter"
	ownershipId="PartnerCenter_Ingestion"
/>
# Microsoft 365 App Compliance program

---
{
   "$schema": "SelfHelpContent",
   "resourceRequired": true,
   "subscriptionRequired": true,
   "title": "Microsoft 365 App Compliance program",
   "fileAttachmentHint": "Please upload any supporting files that can help us better understand your issue (screen recording or a document with steps/screenshots to recreate the issue)",
   "formElements": [
       {
	   "id": "pc_offer_name",
	   "order": 1,
	   "controlType": "textbox",
	   "displayLabel": "Offer name",
	   "watermarkText": "Please provide the Offer name",
	   "required": true
       },
       {
	   "id": "pc_offer_type",
       "order": 2,
	   "controlType": "dropdown",
	   "displayLabel": "Office Store Offer Type:",
       "watermarkText":"Please select the Office Store Offer Type from the below list",
	   "dropdownOptions": [
	       {
		   "value": "office_add_in",
		   "text": "Office add-ins"
	       },
	       {
		   "value": "sharepoint_solution",
		   "text": "SharePoint Solution"
	       },
	       {
		   "value": "teams_app",
		   "text": "Teams App"
	       },
	       {
		   "value": "dont_know_answer",
		   "text": "Not sure"
	       }
	       ],
	   "required": true
       },
       {
	   "id": "pc_application_type",
       "order": 3,
	   "controlType": "dropdown",
	   "displayLabel": "Application",
       "watermarkText":"Please select the Application from the below list",
	   "dropdownOptions": [
	       {
		   "value": "excel_app",
		   "text": "Excel"
	       },
	       {
	       	   "value": "onenote_app",
		   "text": "OneNote"
		},
	       {
		   "value": "outlook_app",
		   "text": "Outlook"
	       },
	       {
		   "value": "powerpoint_app",
		   "text": "PowerPoint"
	       },
	       {
		   "value": "project_app",
		   "text": "Project"
	       },
	       {
		   "value": "sharepoint_app",
		   "text": "SharePoint"
	       },
	       {
		   "value": "teams_app",
		   "text": "Teams"
	       },
	       {
		   "value": "word_app",
		   "text": "Word"
	       },
	       {
		   "value": "others_value",
		   "text": "Others"
	       }
	       ],
	   "required": false
       },
       {
	   "id": "problem_start_time",
	   "order": 4,
	   "controlType": "datetimepicker",
	   "displayLabel": "Submission Date",
	   "watermarkText": "When did your issue begin?",
	   "required": true
       },
       {
	   "id": "problem_description",
	   "order": 5,
	   "controlType": "multilinetextbox",
	   "displayLabel": "Details",
	   "watermarkText": "Please provide any other additional information about your issue",
	   "required": true,
	   "useAsAdditionalDetails": true
       }
   ]
}
---
