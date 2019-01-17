<properties
	pageTitle="Request for Cancellation of a Subscription"
	description="Request for Cancellation of a Subscription"
	articleId="requestforcancellationofasubscriptionthirdpartypurchase"
	ms.author="prdasneo"
	authors="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32549163"
	productPesIds="15660"
	cloudEnvironments="public"
	schemaVersion="1"
/>

# Third Party Purchase
---
{
	"resourceRequired": false,
	"title": "Thirdparty purchase",
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
					"text": "Name of service"
				}, {
					"text": "Error message encountered while cancelling the subscription"
				}, {
					"text": "Cancellation Reason"
				}
			]
		}
	]
}
---
