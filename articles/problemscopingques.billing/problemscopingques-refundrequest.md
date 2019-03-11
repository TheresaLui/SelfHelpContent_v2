<properties
	pageTitle="Refund Request"
	description="Refund Request"
	articleId="refundrequest"
	ms.author="prdasneo"
	authors="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32454868"
	productPesIds="15659"
	cloudEnvironments="public"
	schemaVersion="1"
/>

# Refund Request
---
{
	"resourceRequired": false,
	"title": "Refund Request",
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
					"text": "Refund amount"
				}, {
					"text": "Reason for refund request"
				}
			]
		}
	]
}
---
