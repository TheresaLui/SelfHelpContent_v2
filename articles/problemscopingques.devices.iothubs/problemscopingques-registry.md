<properties
	pageTitle="Device identity registry issues"
	description="Device identity registry issues for IoT Hub scoping questions"
	authors="jlian"
	ms.author="jlian"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630542"
	productPesIds="15946"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="78ba0c10-b1aa-4dbd-87cb-008d03396beb"
	ownershipId="AzureIot_IotHub"
/>
# Device identity registry issues
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": false,
  "resourceRequired": false,
  "title": "Device identity registry issues",
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
      "id": "errors",
      "order": 10,
      "controlType": "textbox",
      "displayLabel": "What error did you see?",
      "watermarkText": "Example: 429001 ThrottlingException",
      "required": false
    },
    {
      "id": "programmatically",
      "order": 15,
      "controlType": "dropdown",
      "displayLabel": "Are you performing device identity registry operations programmatically (API, SDK, PowerShell, or CLI)?",
      "watermarkText": "Choose an option",
      "dropdownOptions": [
        {
          "value": "Yes",
          "text": "Yes"
        },
        {
          "value": "No",
          "text": "No"
        },
        {
          "value": "dont_know_answer",
          "text": "Other, don't know, or not applicable"
        }
      ],
      "required": false
    },
    {
      "id": "code",
      "order": 20,
      "controlType": "multilinetextbox",
      "visibility": "programmatically == Yes",
      "displayLabel": "Can you share the code snippet or command used?",
      "watermarkText": "Paste here",
      "required": false
    }
  ]
}
---