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
	   "id": "pc_publisher_id",
	   "order": 1,
	   "controlType": "textbox",
	   "displayLabel": "Publisher ID",
	   "watermarkText": "Please provide the Publisher ID",
	   "infoBalloonText": "Open another Partner Center tab and follow these instructions: Select the cog wheel icon on the top right, then Account Settings. Under Organization Profile select Identifiers, the Seller ID & Publisher ID are listed under the Commercial Marketplace section.",
	   "required": true
	},
	{
	   "id": "pc_publisher_name",
	   "order": 2,
	   "controlType": "textbox",
	   "displayLabel": "Publisher name",
	   "watermarkText": "Please provide the Publisher name",
	   "required": false
       },
       {
	   "id": "pc_offer_name",
	   "order": 3,
	   "controlType": "textbox",
	   "displayLabel": "Offer name",
	   "watermarkText": "Please provide the Offer name",
	   "required": false
       },
       {
	   "id": "pc_offer_type",
       "order": 4,
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
       "order": 5,
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
	   "order": 7,
	   "controlType": "datetimepicker",
	   "displayLabel": "Submission Date",
	   "watermarkText": "When did your issue begin?",
	   "required": true
       },
       {
	   "id": "problem_description",
	   "order": 8,
	   "controlType": "multilinetextbox",
	   "displayLabel": "Details",
	   "watermarkText": "Please provide any other additional information about your issue",
	   "required": true,
	   "useAsAdditionalDetails": true
       }
   ]
}
---
