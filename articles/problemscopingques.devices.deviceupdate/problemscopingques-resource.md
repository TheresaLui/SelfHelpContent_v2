<properties
	pageTitle="Device Update for Azure IoT Hub resource issues"
	description="Scoping questions for Device Update for Azure IoT Hub resource issues"
	authors="lichris"
	ms.author="lichris"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32787855"
	productPesIds="17393"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="device-update-resource"
	ownershipId="EDS_AzureDeviceUpdate"
/>
# Device Update resource issues
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": false,
  "resourceRequired": false,
  "title": "Device Update for Azure IoT Hub resource issues",
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
      "watermarkText": "Example: 500001 ServerError",
      "required": false
    }
  ]
}
---