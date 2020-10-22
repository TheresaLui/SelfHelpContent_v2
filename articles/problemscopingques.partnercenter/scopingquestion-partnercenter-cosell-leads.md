<properties
       pageTitle="Leads"
       description="Leads"
       authors="a-crmire"
       ms.author="a-crmire"
       selfHelpType="problemScopingQuestions"
       supportTopicIds="32749481,32749484,32749486"
       productPesIds="17004"
       cloudEnvironments="public, fairfax, blackforest, mooncake, ussec, usnat"
       schemaVersion="1"
       articleId="problemscopingques_partnercenter-cosell-leads" 
       clientIds="partnercenter"
       ownershipId="PartnerCenter_PartnerCenter_Cosell"
/>
# Leads

---
{
   "$schema": "SelfHelpContent",
   "resourceRequired": true,
   "subscriptionRequired": true,
   "title": "Cosell Leads",
   "fileAttachmentHint": "Please upload any supporting files that can help us better understand your issue (screen recording, HTTP archive file or document with steps to recreate the issue)",
   "formElements": [
       {
	   "id": "business_profile_name",
	   "order": 1,
	   "controlType": "textbox",
	   "displayLabel": "Business Profile name",
	   "watermarkText": "Please provide the Business Profile name",
	   "required": false
       },
      {
	   "id": "business_profile_location",
	   "order": 2,
	   "controlType": "textbox",
	   "displayLabel": "Business Profile location",
	   "watermarkText": "Please provide the Business Profile location",
	   "required": false
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
       "id": "learn_more_text1",
       "order": 4,
       "controlType": "infoblock",
       "content": "<a href='https://docs.microsoft.com/azure/azure-portal/capture-browser-trace'>To help with troubleshooting please follow the HTTP archive file instructions and upload below</a>"
       },
       {
	   "id": "problem_start_time",
	   "order": 7,
	   "controlType": "datetimepicker",
	   "displayLabel": "Start Date",
	   "watermarkText": "When did your issue begin?",
	   "required": true
       }
   ]
}
---
