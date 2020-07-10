<properties
	pageTitle="Event Grid issues"
	description="Event Grid issues for IoT Hub scoping questions"
	authors="jlian"
	ms.author="jlian"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32680886"
	productPesIds="15946"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="3db7fbec-e670-4c45-a632-d54a39722ad1"
	ownershipId="AzureIot_IotHub"
/>
# Event Grid issues
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": false,
  "resourceRequired": false,
  "title": "Event Grid issues",
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
      "id": "event_type",
      "order": 5,
      "controlType": "multiselectdropdown",
      "displayLabel": "What type of event are you having issues with?",
      "watermarkText": "Choose an option",
      "dropdownOptions": [
        {
          "value": "Device Created",
          "text": "Device Created"
        },
        {
          "value": "Device Deleted",
          "text": "Device Deleted"
        },
        {
          "value": "Device Connected",
          "text": "Device Connected"
        },
        {
          "value": "Device Disconnected",
          "text": "Device Disconnected"
        },
        {
          "value": "Device Telemetry",
          "text": "Device Telemetry"
        },
        {
          "value": "dont_know_answer",
          "text": "Other, don't know, or not applicable"
        }
      ],
      "required": true
    },
    {
      "id": "problem_description",
      "order": 10,
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
    }
  ]
}
---