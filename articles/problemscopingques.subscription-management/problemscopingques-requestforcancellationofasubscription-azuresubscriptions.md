<properties
	pageTitle="Request for Cancellation of a Subscription"
	description="Request for Cancellation of a Subscription"
	articleId="requestforcancellationofasubscriptionazuresubscriptions"
	ms.author="prdasneo"
	authors="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32549156"
	productPesIds="15660"
	cloudEnvironments="public"
	schemaVersion="1"
/>

# Azure Subscription Cancellation
---
{
	"resourceRequired": false,
	"title": "Azure subscriptions",
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
					"text": "Error message encountered while cancelling the subscription"
				}, {
					"text": "Cancellation Reason"
				}
			]
		}
	]
}
---
