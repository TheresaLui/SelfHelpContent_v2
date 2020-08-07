<properties
	pageTitle="Throttling or quota hit"
	description="Throttling or quota hit for IoT Hub scoping questions"
	authors="jlian"
	ms.author="jlian"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630567"
	productPesIds="15946"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="7348b913-2ced-401c-9110-9cda48f6d74c"
	ownershipId="AzureIot_IotHub"
/>
# Throttling or quota hit
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": false,
  "resourceRequired": false,
  "title": "Throttling or quota hit",
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
      "watermarkText": "Example: 429001 ThrottlingException, 403002 IotHubQuotaExceeded",
      "required": false
    },
    {
      "id": "feature",
      "order": 15,
      "controlType": "multiselectdropdown",
      "displayLabel": "What feature were you using when you were throttled or hit quota?",
      "watermarkText": "Choose an option",
      "dropdownOptions": [
        {
          "value": "Twin (device and module) operations",
          "text": "Twin (device and module) operations"
        },
        {
          "value": "Device to cloud sends",
          "text": "Device to cloud sends"
        },
        {
          "value": "Identity registry operations",
          "text": "Identity registry operations"
        },
        {
          "value": "New device connections",
          "text": "New device connections"
        },
        {
          "value": "Cloud-to-device sends",
          "text": "Cloud-to-device sends"
        },
        {
          "value": "Queries",
          "text": "Queries"
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