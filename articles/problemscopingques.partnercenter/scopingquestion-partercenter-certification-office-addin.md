<properties
       pageTitle="Marketplace Certification Office Add-in issue"
       description="Marketplace Certification Office Add-in ticketing intake form"
       authors="A-COFLOR"
       ms.author="A-COFLOR"
       selfHelpType="problemScopingQuestions"
       supportTopicIds="32728183"
       productPesIds="17009"
       cloudEnvironments="public, fairfax, blackforest, mooncake, ussec, usnat"
       schemaVersion="1"
       articleId="problemscopingques_partnercenter_certification_office_addin"
       clientIds="partnercenter"
	ownershipId="PartnerCenter_Offer_Certification"
/>
# Certification issue Office Add-in

---
{
   "$schema": "SelfHelpContent",
   "resourceRequired": true,
   "subscriptionRequired": true,
   "title": "Marketplace Certification Issue",
   "fileAttachmentHint": "Please upload any supporting files that can help us better understand your issue (e.g. rejection report)",
   "formElements": [
       {
	   "id": "pc_isv_offer_type",
	   "order": 1,
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
	   "order": 2,
	   "controlType": "textbox",
	   "displayLabel": "Offer ID",
	   "watermarkText": "Please provide the Offer ID",
	   "required": true
       },
       {
	   "id": "pc_isv_offer_name",
	   "order": 3,
	   "controlType": "textbox",
	   "displayLabel": "Offer Name",
	   "watermarkText": "Please provide the Offer Name",
	   "required": false
       },
       {
	   "id": "business_justification",
	   "order": 4,
	   "controlType": "multilinetextbox",
	   "displayLabel": "Business justification",
	   "watermarkText": "Expediting the certification process is not supported unless there is a strong business justification",
	   "required": false
       },
       {
	   "id": "offer_submit_date",
	   "order": 5,
	   "controlType": "datetimepicker",
	   "displayLabel": "Partner Center Offer submitted date",
	   "watermarkText": "Please select the Offer submitted date",
	   "required": true
       },
       {
	   "id": "pc_isv_client_type",
	   "order": 6,
	   "controlType": "dropdown",
	   "displayLabel": "Client Type",
       "watermarkText":"Please select the Client Type from the below list",
	   "dropdownOptions": [
	       {
		   "value": "excel_client",
		   "text": "Excel"
	       },
	       {
		   "value": "onenote_client",
		   "text": "OneNote"
	       },
	       {
		   "value": "outlook_client",
		   "text": "Outlook"
	       },
	       {
		   "value": "powerBI_visual_client",
		   "text": "PowerBI Visual"
	       },
	       {
		   "value": "powerpoint_client",
		   "text": "PowerPoint"
	       },
	       {
		   "value": "project_client",
		   "text": "Project"
	       },
	       {
		   "value": "sharepoint_client",
		   "text": "SharePoint"
	       },
	       {
		   "value": "word_client",
		   "text": "Word"
	       },
	       {
		   "value": "dont_know_answer",
		   "text": "Other"
	       }
	       ],
	   "required": true
       },
       {
	   "id": "client_version",
	   "order": 7,
	   "controlType": "textbox",
	   "displayLabel": "Client Version",
	   "watermarkText": "Please provide the Client Version",
       "infoBalloonText": "In order to find the client version please go to File - Account - About. You can find an example <a href='https://support.microsoft.com/office/what-version-of-outlook-do-i-have-b3a9568c-edb5-42b9-9825-d48d82b2257c'>HERE</a>",
	   "required": false
       },
       {
	   "id": "related_policy",
	   "order": 8,
	   "controlType": "textbox",
	   "displayLabel": "Related Policy",
	   "watermarkText": "Please provide the Related Policy",
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
