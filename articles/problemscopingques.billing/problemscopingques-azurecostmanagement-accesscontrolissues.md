<properties
	pageTitle="Azure Cost Management"
	description="Azure Cost Management"
	articleId="azurecostmanagement"
	ms.author="prdasneo"
	authors="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32615278,32615287,32615306"
	productPesIds="15659"
	cloudEnvironments="public"
	schemaVersion="1"
/>

# Azure Cost Management
---
{
	"resourceRequired": false,
	"title": "Azure Cost Management",
	"fileAttachmentHint": "",
	"formElements": [
      {
      "id": "problem_start_time",
      "visibility": null,
      "order": 2,
      "controlType": "datetimepicker",
      "displayLabel": "When did the problem start?",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "required": true,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 0
  },
  {
			"id": "problem_description",
			"order": 1,
			"controlType": "multilinetextbox",
			"displayLabel": "Please provide the following:",
			"required": true,
			"useAsAdditionalDetails": true,
			"hints": [{
					"text": "Subscription ID"
				}, {
					"text": "Email ID accessing the subscription"
				}, {
					"text": "Screenshot of the error"
				}
			]
		}
	]
}
---
