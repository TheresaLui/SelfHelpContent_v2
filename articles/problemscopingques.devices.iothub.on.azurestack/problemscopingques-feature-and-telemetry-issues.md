<properties
  articleId="problemscopingques-feature-and-telemetry-issues"
  pageTitle="Scoping questions - Issues related to Hub on Stack telemetry issues"
  description="Scoping questions to troubleshoot the issues related to telemetry issues"
  authors="camanle"
  authoralias="camanle"
  ms.author="camanle"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32782336, 32782342, 32782329, 32782328, 32782330, 32782340"
  productPesIds="17381"
  cloudEnvironments="public, Fairfax, usnat, ussec, mooncake"
  schemaVersion="1"
  ownershipId="AzureIot_IotHub"
/>
# Issues related to Hub on Stack telemetry issues
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": true,
  "resourceRequired": true,
  "title": "Issues related to Hub on Stack operations",
  "fileAttachmentHint": "Please provide a screenshot of any errors",
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
      "useAsAdditionalDetails": false,
      "required": false
    },
    {
      "id": "device_id",
      "order": 6,
      "controlType": "textbox",
      "displayLabel": "Can you provide a list of affected device ids?",
      "useAsAdditionalDetails": false,
      "required": false
    },
    {
      "id": "protocol",
      "order": 7,
      "controlType": "radiobuttongroup",
      "displayLabel": "What protocol are you using?",
      "radioButtonOptions": [
        {
          "value": "MQTT",
          "text": "MQTT"
        },
        {
          "value": "AMQP",
          "text": "AMQP"
        },
        {
          "value": "HTTPS",
          "text": "HTTPS"
        },
        {
          "value": "AMQP over Websockets",
          "text": "AMQP over Websockets"
        },
        {
          "value": "MQTT over Websockets",
          "text": "MQTT over Websockets"
        }
      ],
      "required": false
    },
    {
      "id": "device_sdk",
      "order": 8,
      "controlType": "multilinetextbox",
      "displayLabel": "If you are using a device SDK, can you specify the language and version",
      "watermarkText": "Examples - Node 1.17.3, C# 1.32, etc)",
      "useAsAdditionalDetails": false,
      "required": false
    },
    {
      "id": "problem_description",
      "order": 9,
      "controlType": "multilinetextbox",
      "displayLabel": "Problem description",
      "watermarkText": "Provide additional information about your issue",
      "useAsAdditionalDetails": true,
      "required": true
    }
  ]
}
---