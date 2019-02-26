<properties
	pageTitle="Need a Copy of My Bill and Usage"
	description="Need a Copy of My Bill and Usage"
	articleId="needacopyofmybillandusage"
	ms.author="prdasneo"
	authors="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32454862"
	productPesIds="15659"
	cloudEnvironments="public"
	schemaVersion="1"
/>

# Need a Copy of My Bill and Usage
---
{
	"resourceRequired": false,
	"title": "Need a Copy of My Bill and Usage",
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
					"text": "Email ID used to download report"
				}, {
					"text": "Error message (if applicable)"
				}
			]
		}
	]
}
---
