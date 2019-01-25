<properties
	pageTitle="Add or Edit VAT TAX ID or PO Number"
	description="Add or Edit VAT TAX ID or PO Number"
	articleId="addoreditvattaxidorponumber"
	ms.author="prdasneo"
	authors="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32454917"
	productPesIds="15660"
	cloudEnvironments="public"
	schemaVersion="1"
/>

# Add or Edit VAT TAX ID or PO Number
---
{
	"resourceRequired": false,
	"title": "Add or Edit VAT TAX ID or PO Number",
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
					"text": "Please enter your VAT, TAX ID, or PO Number"
				}
			]
		}
	]
}
---
