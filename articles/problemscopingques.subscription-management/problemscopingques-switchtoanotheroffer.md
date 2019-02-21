<properties
	pageTitle="Switch to Another Offer"
	description="Switch to Another Offer"
	authors="prdasneo"
	ms.author="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32454938"
	productPesIds="15660"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="switchtoanotheroffer"
/>


# Switch to Another Offer
---
{
    "resourceRequired": false,
    "title": "Switch to Another Offer",
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
					"text": "The solution provided is limited to Pay As You Go only. To Convert to any other offer, please provide:"
				},
				{
					"text": "Subscription ID"
				},
				{
					"text": "New Offer type to convert to"
				}
			]
		}
	]
}
---
