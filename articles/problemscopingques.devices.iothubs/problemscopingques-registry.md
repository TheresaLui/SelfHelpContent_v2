<properties
	pageTitle="Device identity registry issues"
	description="Device identity registry issues for IoT Hub scoping questions"
	authors="jlian"
	ms.author="jlian"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630542"
	productPesIds="15946"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake"
	schemaVersion="1"
	articleId="78ba0c10-b1aa-4dbd-87cb-008d03396beb"
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
      "id": "errors",
      "order": 2,
      "controlType": "textbox",
      "displayLabel": "What error did you see?",
      "watermarkText": "Example: 429001 ThrottlingException, 403002 IotHubQuotaExceeded",
      "required": true
    },
    {
      "id": "programmatically",
      "order": 3,
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
      "required": true
    },
    {
      "id": "code",
      "order": 4,
      "controlType": "multilinetextbox",
      "visibility": "programmatically == Yes",
      "displayLabel": "Can you share the code snippet or command used?",
      "watermarkText": "Paste here",
      "required": true
    },
    {
      "id": "problem_description",
      "order": 10,
      "controlType": "multilinetextbox",
      "displayLabel": "Description",
      "watermarkText": "Provide additional information about your issue",
      "required": true,
      "useAsAdditionalDetails": true
    }
  ]
}
---