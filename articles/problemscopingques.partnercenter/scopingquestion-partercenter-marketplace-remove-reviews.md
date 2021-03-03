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
# Remove reviews
---
{
   "$schema": "SelfHelpContent",
   "resourceRequired": true,
   "subscriptionRequired": true,
   "title": "Remove reviews from Marketplace store",
   "fileAttachmentHint": "Upload any supporting files (screenshot of the review to remove) that can help us understand your issue.",
   "formElements": [
       {
       "id": "learn_more_text1",
       "visibility": null,
       "order": 1,
       "controlType": "infoblock",
       "content": "For a better analysis and a faster resolution please attach a screenshot of the review to be removed in the Upload section above"
       },
       {
       "id": "pc_isv_offer_name",
       "order": 2,
       "visibility": null,
       "controlType": "textbox",
       "displayLabel": "Offer Name",
       "watermarkText": "Please provide the Offer Name",
       "required": false
       },
       {
       "id": "pc_isv_offer_id",
       "order": 3,
       "visibility": null,
       "controlType": "textbox",
       "displayLabel": "Offer ID",
       "watermarkText": "Please provide the Offer ID",
       "required": true
       },
       {
       "id": "pc_isv_offer_type",
       "order": 4,
       "visibility": null,
       "controlType": "dropdown",
       "displayLabel": "Offer Type",
       "watermarkText": "Please select the Offer Type from the below list",
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
	"text": "Dynamics 365 Business Central offer"
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
	}],
	"required": false
       },
       {
       "id": "business_just",
       "order": 5,
       "visibility": null,
       "controlType": "dropdown",
       "displayLabel": "Business justification for removal",
       "watermarkText": "Please select a Business justification from the below list",
       "dropdownOptions": [
       	{
	"value": "offensive_content",
	"text": "Offensive content"
	},
	{
	"value": "spam_advertising",
	"text": "Spam or advertising"
	},
	{
	"value": "invalid_review",
	"text": "Invalid review"
	},
	{
	"value": "dont_know_answer",
	"text": "Other"
	}],
	"required": true
       },
       {
       "id": "additional_bussjust",
       "order": 6,
       "visibility": "business_just==dont_know_answer",
       "controlType": "multilinetextbox",
       "displayLabel": "Business justification",
       "watermarkText": "Removing a review from Marketplace store fronts requires a business justification. Please provide a reason for why the review should be removed.",
       "required": true
       },
       {
       "id": "offer_url",
       "order": 7,
       "visibility": null,
       "controlType": "textbox",
       "displayLabel": "Storefront offer URL",
       "watermarkText": "Please provide the URL of offer in storefront where review is associated",
       "required": true
       },
       {
       "id": "user_review_date",
       "order": 8,
       "visibility": null,
       "controlType": "datetimepicker",
       "displayLabel": "When was the review posted?",
       "watermarkText": "When was the review posted?",
       "required": false
       },
       {
       "id": "review_title",
       "order": 9,
       "visibility": null,
       "controlType": "textbox",
       "displayLabel": "Review title",
       "watermarkText": "Please provide the Review title",
       "required": false
       },
       {
       "id": "file_attached",
       "order": 10,
       "visibility": null,
       "controlType": "dropdown",
       "displayLabel": "Have you attached a screenshot (in the Upload section above) of the exact review to be removed?",
       "watermarkText": "Please select from the below list",
	   "dropdownOptions": [
	       {
		   "value": "Yes",
		   "text": "Yes"
	       },
	       {
		   "value": "No",
		   "text": "No"
	       }
	       ],
	   "required": false
       },
       {
       "id": "learn_more_text2",
       "visibility": "attached_file==No",
       "order": 11,
       "controlType": "infoblock",
       "content": "For a better analysis and a faster resolution please attach a screenshot of the review to be removed in the Upload section above"
       },
       {
       "id": "problem_description",
       "order": 12,
       "controlType": "multilinetextbox",
       "displayLabel": "Details",
       "watermarkText": "Please provide any other additional information about your issue",
       "required": true,
       "useAsAdditionalDetails": true
       },
       {
       "id": "problem_start_time",
       "order": 13,
       "controlType": "datetimepicker",
       "displayLabel": "Start Date",
       "watermarkText": "When did your issue begin?",
       "required": true
       }
   ]
}
---
