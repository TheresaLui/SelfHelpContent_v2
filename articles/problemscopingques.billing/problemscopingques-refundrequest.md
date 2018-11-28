<properties
	pageTitle="Refund Request"
	description="Refund Request"
	articleId="refundrequest"
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
					"text": "Refund amount"
				}, {
					"text": "Reason for refund request"
				}
			]
		}
	]
}
---
