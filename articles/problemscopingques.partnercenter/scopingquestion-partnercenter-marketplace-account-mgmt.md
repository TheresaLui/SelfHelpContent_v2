<properties
       pageTitle="Marketplace Account Management issues"
       description="Marketplace Account Management issues ticketing intake form"
       authors="A-COFLOR"
       ms.author="A-COFLOR"
       selfHelpType="problemScopingQuestions"
       supportTopicIds="32728050,32728232"
       productPesIds="17000"
       cloudEnvironments="public, fairfax, blackforest, mooncake, ussec, usnat"
       schemaVersion="1"
       articleId="problemscopingques_partnercenter_acctmgt_issue" 
       clientIds="partnercenter"
	ownershipId="PartnerCenter_Accounts_Onboarding_Access"
/>
# Account Management Issues

---
{
   "$schema": "SelfHelpContent",
   "resourceRequired": true,
   "subscriptionRequired": true,
   "title": "Marketplace Account Management Issues",
   "fileAttachmentHint": "Please upload any supporting files that can help us better understand your issue (screen recording or a document with steps to recreate the issue)",
   "formElements": [
       {
	   "id": "tenant_id",
	   "order": 1,
	   "controlType": "textbox",
	   "displayLabel": "Tenant ID",
	   "watermarkText": "Please provide the Tenant ID - if you are adding Owner, Users or Managers",
	   "required": false
       },
       {
       "id": "learn_more_text1",
       "order": 2,
       "controlType": "infoblock",
       "content": "<a href='https://docs.microsoft.com/azure/marketplace/find-tenant-object-id#find-tenant-id'>How to find Tenant ID association for debugging purposes</a>"
       },
       {
	   "id": "object_id",
	   "order": 3,
	   "controlType": "textbox",
	   "displayLabel": "Object ID",
	   "watermarkText": "Please provide the Object ID - if this is regarding a Registration query",
	   "required": false
       },
       {
       "id": "learn_more_text2",
       "order": 4,
       "controlType": "infoblock",
       "content": "<a href='https://docs.microsoft.com/azure/marketplace/find-tenant-object-id#find-user-object-id'>How to find Object ID association for debugging purposes</a>"
       },
       {
	   "id": "additional_email(s)_for_notification",
	   "order": 5,
	   "controlType": "textbox",
	   "displayLabel": "Additional email(s) for notification",
	   "watermarkText": "Please add name@emailaddress.com here if you'd like us to include others on the SR communications.",
	   "required": false
       },
       {
	   "id": "problem_description",
	   "order": 6,
	   "controlType": "multilinetextbox",
	   "displayLabel": "Details",
	   "watermarkText": "Please provide any other additional information about your issue",
	   "required": true,
	   "useAsAdditionalDetails": true
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
