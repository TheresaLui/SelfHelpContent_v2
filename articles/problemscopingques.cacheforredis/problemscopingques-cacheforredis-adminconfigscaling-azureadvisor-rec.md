<properties
	pageTitle="Azure Advisor recommendation"
	description="Azure Advisor recommendation"
	service="microsoft.cache"
	resource="redis"
	authors="johnnygetHub"
	ms.author="johnnyc"
	displayOrder=""
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32690904"
	resourceTags=""
	productPesIds="14783"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
    schemaVersion="1"
	articleId="8f0d05aa-d988-4078-9fa1-6efe8ff4a83f"
	ownershipId="RedisCache_RedisCache"
/>
# Azure Advisor recommendation
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": true,
  "resourceRequired": true,
	"title": "Slow virtual machine",
	"fileAttachmentHint": "",
	"formElements": [
		{
			"id": "slow_vm_determination",
			"order": 1,
			"controlType": "dropdown",
			"infoBalloonText": "string",
			"displayLabel": "Is this a yes or no question?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [
				{
					"value": "Yes",
					"text": "Yes"
				}, {
					"value": "No",
					"text": "No"
				}, {
					"value": "dont_know_answer",
					"text": "Don't Know"
				}
			],
			"required": false
		}, {
			"id": "problem_start_time",
			"order": 2,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
		}, {
			"id": "applications_on_vm",
			"order": 3,
			"controlType": "multiselectdropdown",
			"displayLabel": "Select the applications running on your virtual machine",
			"dropdownOptions": 
			[{
					"value": "CRM Dynamics",
					"text": "CRM Dynamics"
				}, {
					"value": "IIS / Web Front end",
					"text": "IIS / Web Front end"
				}, {
					"value": "MySQL",
					"text": "MySQL"
				}, {
					"value": "Oracle",
					"text": "Oracle"
				}, {
					"value": "Remote Desktop Services",
					"text": "Remote Desktop Services"
				}, {
					"value": "SAP Hanna",
					"text": "SAP Hanna"
				}, {
					"value": "SharePoint",
					"text": "SharePoint"
				}, {
					"value": "SQL",
					"text": "SQL"
				}, {
					"value": "Other (describe below)",
					"text": "Other"
				}
			],
			"required": false
		}, {
			"id": "problem_description",
			"order": 5,
			"controlType": "multilinetextbox",
			"displayLabel": "Details",
			"watermarkText": "Provide additional information about your issue",
			"required": true,
			"useAsAdditionalDetails": true,
			"hints": [{
					"text": "Issue description."
				}, {
					"text": "Name of the virtual machine(s) in the same subscription that you think is faster than the slow virtual machine."
				}
			]
		}, {
			"id": "learn_more_text",
			"order": 6,
			"controlType": "infoblock",
			"content": "<a href='https://jsonlint.com/'>Use this JSON Checker</a> if you are receiving validation errors in your scoping question"
		}
	]
}
---
