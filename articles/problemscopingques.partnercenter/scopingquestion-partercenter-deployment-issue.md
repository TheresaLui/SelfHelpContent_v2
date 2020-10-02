<properties
       pageTitle="Marketplace Deployment issue"
       description="Marketplace Deployment issue ticketing intake form"
       authors="A-COFLOR"
       ms.author="A-COFLOR"
       selfHelpType="problemScopingQuestions"
       supportTopicIds="32728088"
       productPesIds="17006"
       cloudEnvironments="public, fairfax, blackforest, mooncake, ussec, usnat"
       schemaVersion="1"
       articleId="problemscopingques_partnercenter_deployment_issue" 
       clientIds="partnercenter"
	ownershipId="PartnerCenter_Ingestion"
/>
# Deployment Issue

---
{
   "$schema": "SelfHelpContent",
   "resourceRequired": true,
   "subscriptionRequired": true,
   "title": "Marketplace Deployment Issue",
   "fileAttachmentHint": "Please upload any supporting files that can help us better understand your issue (screen recording, HAR file or document with steps to recreate the issue)",
   "formElements": [
       {
	   "id": "pc_isv_publisher_name",
       	   "visibility": null,
	   "order": 1,
	   "controlType": "textbox",
	   "displayLabel": "Publisher name",
	   "watermarkText": "Please provide the publisher name.",
	   "required": true
       },
       {
	   "id": "pc_isv_publisher_id",
       	   "visibility": null,
	   "order": 2,
	   "controlType": "numerictextbox",
	   "displayLabel": "Publisher ID.",
	   "watermarkText": "In Partner Center select Settings then Developer settings.",
	   "required": false
       },
       {
	   "id": "pc_isv_seller_id",
           "visibility": null,
	   "order": 3,
	   "controlType": "numerictextbox",
	   "displayLabel": "Please provide the seller ID.",
	   "watermarkText": "In Partner Center select Settings then Developer settings.",
	   "required": true
       },
       {
	   "id": "pc_isv_offer_type",
           "visibility": null,
	   "order": 4,
	   "controlType": "dropdown",
	   "displayLabel": "Offer Type:",
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
           "visibility": null,
	   "order": 5,
	   "controlType": "textbox",
	   "displayLabel": "Offer ID",
	   "watermarkText": "Please provide the Offer ID.",
	   "required": false
       },
       {
	   "id": "pc_isv_offer_name",
           "visibility": null,
	   "order": 6,
	   "controlType": "textbox",
	   "displayLabel": "Offer Name",
	   "watermarkText": "Please provide the Offer Name.",
	   "required": false
       },
       {
	   "id": "pc_isv_offer_private",
           "visibility": null,
	   "order": 7,
	   "controlType": "dropdown",
	   "displayLabel": "Is the offer for Private/Preview audience?",
           "watermarkText":"Please select",
	   "dropdownOptions": [
	       {
		   "value": "PrivatePreview_yes",
		   "text": "Yes"
	       },
	       {
		   "value": "PrivatePreview_no",
		   "text": "No"
	       }],
	   "required": false
       },
       {
	   "id": "pc_isv_private_preview",
           "visibility": "pc_isv_offer_private == PrivatePreview_yes",
	   "order": 8,
	   "controlType": "textbox",
	   "displayLabel": "Please provide additional details",
	   "watermarkText": "Person facing the issue, Subscription ID",
	   "required": false
       },
       {
	   "id": "additional_emails_for_notification",
           "visibility": null,
	   "order": 9,
	   "controlType": "textbox",
	   "displayLabel": "Additional email(s) for notification",
	   "watermarkText": "Please add name@emailaddress.com here if you'd like us to include others on the SR communications.",
	   "required": false
       },
       {
	   "id": "problem_start_time",
           "visibility": null,
	   "order": 10,
	   "controlType": "datetimepicker",
	   "displayLabel": "Start Time",
	   "watermarkText": "When did your issue begin?",
	   "required": true
       },
       {
	   "id": "problem_description",
           "visibility": null,
	   "order": 11,
	   "controlType": "multilinetextbox",
	   "displayLabel": "Details",
	   "watermarkText": "Please provide any other additional information about your issue",
	   "required": true,
	   "useAsAdditionalDetails": true
       },
       {
       "id": "learn_more_text",
       "visibility": null,
       "order": 12,
       "controlType": "infoblock",
       "content": "To help with troubleshooting please follow the <a href='https://docs.microsoft.com/azure/marketplace/partner-center-portal/support#record-issue-details-with-a-har-file'>Network trace (HAR) file instructions</a> and add the HAR file in the Upload section below"
       }
   ]
}
---
