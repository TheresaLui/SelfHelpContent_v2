<properties
       pageTitle="Update MPN ID to help with Co-sell offer setup"
       description="Co-sell offer setup issues ticketing intake form"
       authors="A-COFLOR"
       ms.author="A-COFLOR"
       selfHelpType="problemScopingQuestions"
       supportTopicIds="32783543"
       productPesIds="17006"
       cloudEnvironments="public, fairfax, blackforest, mooncake, ussec, usnat"
       schemaVersion="1"
       articleId="problemscopingques_partnercenter_cosell_mpnid_offer_setup" 
       clientIds="partnercenter"
	ownershipId="PartnerCenter_Ingestion"
/>
# Co-sell offer setup issues

---
{
   "$schema": "SelfHelpContent",
   "resourceRequired": true,
   "subscriptionRequired": true,
   "title": "Co-sell offer setup issues",
   "fileAttachmentHint": "Please upload any supporting files that can help us better understand your issue (screen recording, error messages encountered or a document with steps to recreate the issue)",
   "formElements": [
       {
	   "id": "seller_id",
	   "order": 1,
	   "controlType": "textbox",
	   "displayLabel": "Seller ID",
	   "watermarkText": "Provide the Seller ID for which the MPN ID is to be updated (required)",
	   "required": false
       },
       {
	   "id": "mpn_id",
	   "order": 2,
	   "controlType": "textbox",
	   "displayLabel": "MPN ID",
	   "watermarkText": "Provide the MPN ID to be updated (required)",
	   "required": true
       },
       {
	   "id": "problem_description",
	   "order": 3,
	   "controlType": "multilinetextbox",
	   "displayLabel": "Details",
	   "watermarkText": "Please provide any other additional information about your issue",
	   "required": true,
	   "useAsAdditionalDetails": true
       },
       {
	   "id": "problem_start_time",
	   "order": 4,
	   "controlType": "datetimepicker",
	   "displayLabel": "Start Date",
	   "watermarkText": "When did your issue begin?",
	   "required": true
       }
   ]
}
---
