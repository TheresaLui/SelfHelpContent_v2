<properties
	pageTitle="Add Edit VAT TAX ID or PO Number"
	description="Add Edit VAT TAX ID or PO Number"
	articleId="addeditvattaxidorponumber-problemscopingquestions"
	ms.author="prdasneo"
	authors="prdasneo"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32632927"
	productPesIds="15659"
	cloudEnvironments="public, Mooncake"
	schemaVersion="1"
/>
#  Add Edit VAT TAX ID or PO Number
---
{
  "resourceRequired": false,
  "title": "Add Edit VAT TAX ID or PO Number",
  "fileAttachmentHint": "",
  "formElements": [
    {
      "id": "problem_start_time",
      "visibility": null,
      "order": 1,
      "controlType": "datetimepicker",
      "displayLabel": "Problem Start Date",
      "required": true
    },
    {
      "id": "taxid_details",
      "order": 2,
      "controlType": "textbox",
      "displayLabel": "VAT, TAX ID or PO Number",
      "watermarkText": "Provide your VAT, TAX ID or PO Number",
      "required": true
    },
    {
      "id": "problem_description",
      "order": 3,
      "controlType": "multilinetextbox",
      "useAsAdditionalDetails": true,
      "displayLabel": "Please provide details about your issue",
      "required": true,
      "hints": [
        {
          "text": "Describe your problem, providing as much detail as possible."
        }
      ]
    }
  ]
}
---
