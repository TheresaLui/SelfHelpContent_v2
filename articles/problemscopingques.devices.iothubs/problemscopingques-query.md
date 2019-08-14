<properties
	pageTitle="Query issues"
	description="Query issues for IoT Hub scoping questions"
	authors="jlian"
	ms.author="jlian"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630560"
	productPesIds="15946"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake"
	schemaVersion="1"
	articleId="37c665a3-932e-410e-9dd8-65eaa33f4d1a"
/>
# Query issues
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": false,
  "resourceRequired": false,
  "title": "Query issues",
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
      "controlType": "multilinetextbox",
      "displayLabel": "What is the query?",
      "watermarkText": "SELECT * FROM devices WHERE properties.reported.telemetryConfig.sendFrequencyInSecs >= 60",
      "required": false
    },
    {
      "id": "source",
      "order": 3,
      "controlType": "dropbox",
      "displayLabel": "How are you issuing the query?",
      "watermarkText": "Choose an option",
      "dropdownOptions": [
        {
          "value": "Portal",
          "text": "Portal"
        },
        {
          "value": "SDK",
          "text": "SDK"
        },
        {
          "value": "PowerShellOrCLI",
          "text": "PowerShell or CLI"
        }
      ],
      "required": false
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