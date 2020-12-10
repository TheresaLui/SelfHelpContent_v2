<properties
  articleId="problemscopingques-devices-crud-issues"
  pageTitle="Scoping questions - Issues related to Hub on Stack device operations and CRUD"
  description="Scoping questions to troubleshoot the issues related to device CRUD features of IoT Hub on Azure Stack"
  authors="camanle"
  authoralias="camanle"
  ms.author="camanle"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32782327"
  productPesIds="17381"
  cloudEnvironments="public, Fairfax, usnat, ussec, mooncake"
  schemaVersion="1"
  ownershipId="AzureIot_IotHub"
/>
# Issues related to Hub on Stack device operations and CRUD
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": true,
  "resourceRequired": true,
  "title": "Issues related to Hub on Stack operations",
  "fileAttachmentHint": "Can you upload code snippet and stack trace using file upload?",
  "formElements": [
    {
      "id": "problem_start_time",
      "order": 1,
      "controlType": "datetimepicker",
      "displayLabel": "When did the problem begin?",
      "required": true
    },
    {
      "id": "stack_environment",
      "order": 2,
      "controlType": "radiobuttongroup",
      "displayLabel": "Which Stack environment are you on?",
      "radioButtonOptions": [
        {
          "value": "Connected",
          "text": "Connected"
        },
        {
          "value": "Disconnected",
          "text": "Disconnected"
        }
      ],
      "required": false
    },
    {
      "id": "authentication",
      "order": 3,
      "controlType": "radiobuttongroup",
      "displayLabel": "Are you using AAD or ADFS?",
      "radioButtonOptions": [
        {
          "value": "AAD",
          "text": "AAD"
        },
        {
          "value": "ADFS",
          "text": "ADFS"
        }
      ],
      "required": false
    },
    {
      "id": "cloud_id",
      "order": 4,
      "controlType": "textbox",
      "displayLabel": "What is the Cloud ID",
      "useAsAdditionalDetails": true,
      "required": true
    },
    {
      "id": "build_version",
      "order": 5,
      "controlType": "textbox",
      "displayLabel": "What is your stack build version?",
      "useAsAdditionalDetails": true,
      "required": false
    },
    {
      "id": "devices_programatically",
      "order": 6,
      "controlType": "radiobuttongroup",
      "displayLabel": "Are you creating devices programmatically? If so can you upload code snippet and stack trace using file upload?",
      "radioButtonOptions": [
        {
          "value": "Yes",
          "text": "Yes"
        },
        {
          "value": "No",
          "text": "No"
        }
      ],
      "required": false
    },
    {
      "id": "problem_description",
      "order": 7,
      "controlType": "multilinetextbox",
      "displayLabel": "Problem description",
      "watermarkText": "Provide additional information about your issue",
      "useAsAdditionalDetails": true,
      "required": true
    }
  ]
}
---