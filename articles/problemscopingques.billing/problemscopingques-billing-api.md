<properties
	pageTitle="Billing API"
	description="Billing API"
	articleId="billingapi"
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
      "hints": [],
      "required": true,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 0
  },
  {
			"id": "additional_details",
			"order": 1,
			"controlType": "multilinetextbox",
			"displayLabel": "Please provide these details",
			"required": false,
			"useAsAdditionalDetails": true,
			"hints": [{
					"text": "Subscription ID"
				}, {
					"text": "Email ID accessing the data"
				}, {
					"text": "Error message"
				}
			]
		}
	]
}
---
