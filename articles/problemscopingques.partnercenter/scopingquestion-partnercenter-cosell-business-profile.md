<properties
       pageTitle="Business profile"
       description="Business profile issue"
       authors="a-crmire"
       ms.author="a-crmire"
       selfHelpType="problemScopingQuestions"
       supportTopicIds="32749459,32728065,32749461"
       productPesIds="17004"
       cloudEnvironments="public, fairfax, blackforest, mooncake, ussec, usnat"
       schemaVersion="1"
       articleId="problemscopingques_partnercenter-cosell_business_profile" 
       clientIds="partnercenter"
	ownershipId="PartnerCenter_Cosell"
/>
# Business profile

---
{
   "$schema": "SelfHelpContent",
   "resourceRequired": true,
   "subscriptionRequired": true,
   "title": "Business profile Issues",
   "fileAttachmentHint": "Please upload any supporting files that can help us better understand your issue (screen recording, HTTP archive file or document with steps to recreate the issue)",
   "formElements": [
       {
	   "id": "business_profile_country",
	   "order": 1,
	   "controlType": "textbox",
	   "displayLabel": "Profile country",
	   "watermarkText": "Business profile country/location for this query",
	   "required": false
       },
       {
	   "id": "business_profile_org_size",
       "order": 2,
	   "controlType": "dropdown",
	   "displayLabel": "Organization size used on the Microsoft Solution Provider page",
       "watermarkText":"Your organization size",
	   "dropdownOptions": [
	       {
		   "value": "1-9_employees",
		   "text": "1-9 employees"
	       },
	       {
		   "value": "10-50_employees",
		   "text": "10-50 employees"
	       },
	       {
		   "value": "51-250",
		   "text": "51-250 employees"
	       },
	       {
		   "value": "251-1000",
		   "text": "251-1000 employees"
	       },
	       {
		   "value": "1001-5000",
		   "text": "1001-5000 employees"
	       },
	       {
		   "value": "5001-10000",
		   "text": "5001-10000 employees"
	       },
	        {
		   "value": "10001-20000",
		   "text": "10001-20000 employees"
	       },
		   {
		   "value": "More",
		   "text": "More than 20000 employees"
	       },
		   {
		   "value": "dont_know_answer",
		   "text": "None selected"
	       }
	       ],
	   "required": true
       },
       {
	   "id": "search_term",
	   "order": 3,
	   "controlType": "textbox",
	   "displayLabel": "Search term (products, services, skills, industries or organization)",
	   "watermarkText": "Search term you used on on the Microsoft Solution Provider page",
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
