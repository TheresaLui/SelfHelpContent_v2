<properties
       pageTitle="Marketplace Other Ingestion issues"
       description="Marketplace Other Ingestion issue ticketing intake form"
       authors="A-COFLOR"
       ms.author="A-COFLOR"
       selfHelpType="problemScopingQuestions"
       supportTopicIds="32743375,32728038,32728094,32728255,32728212,32728225,32728082,32728157,32728108,32728192,32728174,32728121,32728134,32728268,32728283,32728242,32728061,32728037,32728093,32728163,32728224,32728211,32728254,32728191,32728120,32728173,32728133,32728107,32728267,32728282,32728081,32728060,32728241,32728039,32728226,32728213,32728256,32728135,32728164,32728095,32728175,32728193,32728269,32728109,32728122,32728083,32728243,32728284,32728062,32728035,32728091,32728156,32728252,32728222,32728131,32728209,32728171,32728105,32728189,32728265,32728280,32728118,32728079,32728058,32728239"
       productPesIds="17006"
       cloudEnvironments="public, fairfax, blackforest, mooncake, ussec, usnat"
       schemaVersion="1"
       articleId="problemscopingques_partnercenter_ingestion_other"
       clientIds="partnercenter"
	ownershipId="PartnerCenter_Ingestion"
/>
# Other Ingestion Issue

---
{
   "$schema": "SelfHelpContent",
   "resourceRequired": true,
   "subscriptionRequired": true,
   "title": "Marketplace Other Ingestion Issue",
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
	   "id": "pc_isv_offer_id",
	   "visibility": null,
	   "order": 5,
	   "controlType": "textbox",
	   "displayLabel": "Offer ID",
	   "watermarkText": "Please provide the Offer ID",
	   "required": false
       },
       {
	   "id": "pc_isv_offer_type",
	   "visibility": null,
	   "order": 6,
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
	   "id": "pc_isv_offer_name",
	   "visibility": null,
	   "order": 7,
	   "controlType": "textbox",
	   "displayLabel": "Offer Name",
	   "watermarkText": "Please provide the Offer Name",
	   "required": false
       },
       {
	   "id": "pc_isv_offer_status",
	   "visibility": null,
	   "order": 8,
	   "controlType": "dropdown",
	   "displayLabel": "Offer status",
       "watermarkText":"Please select the Offer status from the below list",
	   "dropdownOptions": [
	       {
		   "value": "preview_status",
		   "text": "Preview status"
	       },
	       {
		   "value": "live_status",
		   "text": "Live status"
	       },
           {
		   "value": "signoff_status",
		   "text": "Publisher sign-off status"
	       },
	       {
		   "value": "dont_know_answer",
		   "text": "Not sure"
	       }
	       ],
	   "required": true
       },
       {
	   "id": "pc_isv_private_preview",
	   "visibility": "pc_isv_offer_status==preview_status",
	   "order": 9,
	   "controlType": "textbox",
	   "displayLabel": "Please confirm the email address of the person trying to access the preview link",
	   "watermarkText": "Email address of the person trying to access the preview link",
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
