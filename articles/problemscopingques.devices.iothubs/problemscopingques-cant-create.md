<properties
	pageTitle="Can't create IoT hub"
	description="Can't create IoT hub for IoT Hub scoping questions"
	authors="jlian"
	ms.author="jlian"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630529"
	productPesIds="15946"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="a52dc0cc-c9e5-4971-9e51-4ae943380c6c"
	ownershipId="AzureIot_IotHub"
/>
# Can't create IoT hub
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": false,
  "resourceRequired": false,
  "title": "Can't create IoT hub",
  "fileAttachmentHint": "Upload screenshots of errors if available",
  "formElements": [
    {
      "id": "problem_start_time",
      "order": 1,
      "controlType": "datetimepicker",
      "displayLabel": "When did the problem start?",
      "required": true
    },
    {
      "id": "problem_description",
      "order": 5,
      "controlType": "multilinetextbox",
      "displayLabel": "Description",
      "watermarkText": "Provide additional information about your issue",
      "required": true,
      "useAsAdditionalDetails": true,
      "hints": [
        {
          "text": "Description of the issue and repro steps"
        },
        {
          "text": "Error logs with timestamp (indicate timezone or UTC)"
        }
      ]
    },
    {
      "id": "feature",
      "order": 10,
      "controlType": "dropdown",
      "displayLabel": "Did you have issues with creating or deleting IoT hub?",
      "watermarkText": "Choose an option",
      "dropdownOptions": [
        {
          "value": "Create",
          "text": "Create"
        },
        {
          "value": "Delete",
          "text": "Delete"
        },
        {
          "value": "Update",
          "text": "Update"
        },
        {
          "value": "dont_know_answer",
          "text": "Don't know or not applicable"
        }
      ],
      "required": false
    },
    {
      "id": "errors",
      "order": 15,
      "controlType": "textbox",
      "displayLabel": "What error did you see?",
      "watermarkText": "Paste here",
      "required": false
    },
    {
      "id": "where",
      "order": 20,
      "controlType": "dropdown",
      "displayLabel": "Where did you encounter the issue?",
      "watermarkText": "Choose an option",
      "dropdownOptions": [
        {
          "value": "Azure portal",
          "text": "Azure portal"
        },
        {
          "value": "CLI or PowerShell",
          "text": "CLI or PowerShell"
        },
        {
          "value": "dont_know_answer",
          "text": "Other, don't know, or not applicable"
        }
      ],
      "required": false
    }
  ]
}
---