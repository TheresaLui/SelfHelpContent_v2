<properties
	pageTitle="Move Services to Another Subscription"
	description="Move Services to Another Subscription"
	articleId="moveservicestoanothersubscription"
	ms.author="prdasneo"
	authors="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32454926"
	productPesIds="15660"
	cloudEnvironments="public"
	schemaVersion="1"
/>

# Move Services to Another Subscription
---
{
	"resourceRequired": false,
	"title": "Move Services to Another Subscription",
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
					"text": "Source (FROM) Subscription ID"
				}, {
					"text": "Destination (TO) Subscription ID"
				}, {
					"text": "Move all services or selective services"
				}
			]
		}
	]
}
---
