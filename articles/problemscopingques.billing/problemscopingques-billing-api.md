<properties
	pageTitle="Billing API"
	description="Billing API"
	articleId="billingapi"
	ms.author="prdasneo"
	authors="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32599495"
	productPesIds="15659"
	cloudEnvironments="public"
	schemaVersion="1"
/>

# Billing API
---
{
	"resourceRequired": false,
	"title": "Billing API",
	"fileAttachmentHint": "",
	"formElements": [
      {
      "id": "problem_start_time",
      "visibility": null,
      "order": 4,
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
					"text": "Email ID attempting to access the data"
				}, {
					"text": "Error message"
				}
			]
		}
	]
}
---
