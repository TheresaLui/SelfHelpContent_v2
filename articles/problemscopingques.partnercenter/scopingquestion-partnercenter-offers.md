<properties
	pageTitle="Partner Center Offer Issue"
	description="Partner Center Offer Issue"
	authors="brentserbus"
	ms.author="brserbus"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32635654,32635682,32635686,32635689,32635693"
	productPesIds="15960"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="scopingquestion_partnercenter_offers"
	clientIds="partnercenter"
/>
# Partner Center Offer Issue
---
{
  "resourceRequired": true,
  "subscriptionRequired": true,
  "title": "Partner Center Offer Issue",
  "fileAttachmentHint": "",
  "formElements": [
    {
      "id": "pc_offer_id",
      "order": 1,
      "controlType": "textbox",
      "displayLabel": "Please provide the offer id you are having problems finding.",
      "watermarkText": "Provide the offer id as a GUID",
      "required": false
    },
    {
      "id": "pc_customertenant_id",
      "order": 2,
      "controlType": "textbox",
      "displayLabel": "Please provide the customer tenant id you are purchasing for.",
      "watermarkText": "Provide the customer tenant id as a GUID",
      "required": false
    },
    {
      "id": "pc_offer_type",
      "order": 3,
      "controlType": "dropdown",
      "displayLabel": "What kind of offer is your issue about?",
      "watermarkText": "Select offer type",
      "dropdownOptions": [
        {
          "value": "Commercial",
          "text": "Commercial"
        },
        {
          "value": "Academic",
          "text": "Academic"
        },
        {
          "value": "GCC (Government Community Cloud)",
          "text": "GCC (Government Community Cloud)"
        },
        {
          "value": "Nonprofit",
          "text": "Nonprofit"
        }
      ],
      "required": false
    },
    {
      "id": "problem_description",
      "order": 4,
      "controlType": "multilinetextbox",
      "displayLabel": "Details",
      "watermarkText": "Please provide additional information about your issue",
      "required": true,
      "useAsAdditionalDetails": true
    },
    {
      "id": "problem_start_time",
      "order": 5,
      "controlType": "datetimepicker",
      "displayLabel": "Start Time",
      "watermarkText": "When did your issue begin?",
      "required": true
    }
  ]
}
---
