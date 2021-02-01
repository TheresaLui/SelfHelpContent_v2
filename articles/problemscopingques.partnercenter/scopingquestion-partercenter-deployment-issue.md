<properties
       pageTitle="Marketplace Deployment issue"
       description="Marketplace Deployment issue ticketing intake form"
       authors="A-COFLOR"
       ms.author="A-COFLOR"
       selfHelpType="problemScopingQuestions"
       supportTopicIds="32728088,32728029,32728161,32728219,32728205,32728128,32728248,32728168,32728075,32728185,32728102,32728115,32728236,32728276,32728262,32728055"
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
       "id": "learn_more_text",
       "visibility": null,
       "order": 1,
       "controlType": "infoblock",
       "content": "To help with troubleshooting please follow the <a href='https://docs.microsoft.com/azure/marketplace/partner-center-portal/support#record-issue-details-with-a-har-file'>Network trace (HAR) file instructions</a> and add the HAR file in the Upload section above"
       },
       {
	   "id": "pc_isv_publisher_name",
	   "visibility": null,
	   "order": 2,
	   "controlType": "textbox",
	   "displayLabel": "Publisher name",
	   "watermarkText": "Please provide the Publisher name",
	   "required": false
       },
       {
	   "id": "pc_isv_publisher_id",
	   "visibility": null,
	   "order": 3,
	   "controlType": "textbox",
	   "displayLabel": "Publisher ID",
	   "watermarkText": "Please provide the Publisher ID",
	   "infoBalloonText": "Open another Partner Center tab and follow these instructions: Select the cog wheel icon on the top right, then Account Settings. Under Organization Profile select Identifiers, the Seller ID & Publisher ID are listed under the Commercial Marketplace section.",
	   "required": false
       },
       {
	   "id": "pc_isv_seller_id",
	   "visibility": null,
	   "order": 4,
	   "controlType": "textbox",
	   "displayLabel": "Seller ID",
	   "watermarkText": "Please provide the Seller ID",
	   "infoBalloonText": "Open another Partner Center tab and follow these instructions: Select the cog wheel icon on the top right, then Account Settings. Under Organization Profile select Identifiers, the Seller ID & Publisher ID are listed under the Commercial Marketplace section.",
	   "required": true
       },
       {
	   "id": "pc_isv_offer_type",
	   "visibility": null,
	   "order": 5,
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
	   "visibility": null,
	   "order": 6,
	   "controlType": "textbox",
	   "displayLabel": "Offer ID",
	   "watermarkText": "Please provide the Offer ID",
	   "required": false
       },
       {
	   "id": "pc_isv_offer_name",
	   "visibility": null,
	   "order": 7,
	   "controlType": "textbox",
	   "displayLabel": "Offer Name",
	   "watermarkText": "Please provide the Offer Name",
	   "required": false
       },
       {
	   "id": "pc_isv_offer_private",
	   "visibility": null,
	   "order": 8,
	   "controlType": "dropdown",
	   "displayLabel": "Is the offer for Private/Preview audience?",
           "watermarkText":"Choose from below",
	   "dropdownOptions": [
	       {
	       "value": "PrivatePreview_yes",
	       "text": "Yes"
	       },
	       {
	       "value": "PrivatePreview_no",
	       "text": "No"
	       },
	       {
	       "value": "dont_know_answer",
	       "text": "Not sure"
	       }],
	   "required": true
       },
       {
	   "id": "pc_isv_private_preview",
	   "visibility": "pc_isv_offer_private==PrivatePreview_yes",
	   "order": 9,
	   "controlType": "textbox",
	   "displayLabel": "Please specify who is facing the issue and Subscription ID",
	   "watermarkText": "Person facing the issue, Subscription ID",
	   "required": false
       },
       {
	   "id": "problem_start_time",
	   "visibility": null,
	   "order": 11,
	   "controlType": "datetimepicker",
	   "displayLabel": "Start Date",
	   "watermarkText": "When did your issue begin?",
	   "required": true
       },
       {
	   "id": "problem_description",
	   "visibility": null,
	   "order": 12,
	   "controlType": "multilinetextbox",
	   "displayLabel": "Details",
	   "watermarkText": "Please provide any other additional information about your issue",
	   "required": true,
	   "useAsAdditionalDetails": true
       }
]
}
---
