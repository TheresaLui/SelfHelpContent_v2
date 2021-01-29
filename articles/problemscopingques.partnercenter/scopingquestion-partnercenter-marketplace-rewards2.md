<properties
       pageTitle="Marketplace Rewards issue"
       description="Marketplace Rewards issue ticketing intake form"
       authors="A-COFLOR"
       ms.author="A-COFLOR"
       selfHelpType="problemScopingQuestions"
       supportTopicIds="32740798,32740807,32740795,32740794,32740787,32740783"
       productPesIds="17006"
       cloudEnvironments="public, fairfax, blackforest, mooncake, ussec, usnat"
       schemaVersion="1"
       articleId="problemscoping_partnercenter_marketplace_rewards_issue" 
       clientIds="partnercenter"
	ownershipId="PartnerCenter_Ingestion"
/>
# Marketplace Rewards Issues

---
{
   "$schema": "SelfHelpContent",
   "resourceRequired": true,
   "subscriptionRequired": true,
   "title": "Marketplace Rewards Issue",
   "fileAttachmentHint": "Please upload any supporting files that can help us better understand your issue (screen recording or a document with steps to recreate the issue)",
   "formElements": [
       {
	   "id": "pc_isv_offer_id",
	   "order": 1,
	   "controlType": "textbox",
	   "displayLabel": "Offer ID",
	   "watermarkText": "Please provide the Offer ID.",
	   "required": false
       },
       {
	   "id": "marketing_contact",
       "order": 2,
	   "controlType": "dropdown",
	   "displayLabel": "Marketing contact updated?",
       "watermarkText":"In Partner Center under MPN program section check the Marketing contact under Marketplace Rewards",
	   "dropdownOptions": [
	       {
		   "value": "yes_answer",
		   "text": "Yes"
	       },
	       {
		   "value": "no_answer",
		   "text": "No"
	       },
	       {
		   "value": "dont_know_answer",
		   "text": "Not sure"
	       }
	       ],
	   "required": true
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
	   "id": "problem_description",
	   "order": 4,
	   "controlType": "multilinetextbox",
	   "displayLabel": "Details",
	   "watermarkText": "Please provide any other additional information about your issue",
	   "required": true,
	   "useAsAdditionalDetails": true
       },
       {
	   "id": "problem_start_time",
	   "order": 5,
	   "controlType": "datetimepicker",
	   "displayLabel": "Start Date",
	   "watermarkText": "When did your issue begin?",
	   "required": true
       }
   ]
}
---
