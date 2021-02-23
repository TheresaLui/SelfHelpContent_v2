<properties
	pageTitle="Device Update for Azure IoT Hub import issues"
	description="Scoping questions for Device Update for Azure IoT Hub import issues"
	authors="chrisjlin"
	ms.author="lichris"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32787860, 32787862"
	productPesIds="17393"
  articleId="problemscopingques-import"
	cloudEnvironments="public"
	schemaVersion="1"
	ownershipId="EDS_AzureDeviceUpdate"
/>
# Device Update for Azure IoT Hub import issues
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": false,
  "resourceRequired": false,
  "title": "Issues with Device Update importing",
  "fileAttachmentHint": "Please upload the following if available: import manifest.",
  "formElements": [
    {
      "id": "problem_start_time",
      "order": 1,
      "controlType": "datetimepicker",
      "displayLabel": "When did the problem start?",
      "required": true
    },
    {
      "id": "adu_traceid",
      "order": 2,
      "controlType": "textbox",
      "displayLabel": "What is the Trace ID associated with the attempted import action?",
      "required": true
    },
    {
      "id": "adu_account_name",
      "order": 3,
      "controlType": "textbox",
      "displayLabel": "What is the name of your Device Update account?",
      "required": true
    },
    {
      "id": "adu_instance_name",
      "order": 4,
      "controlType": "textbox",
      "displayLabel": "What is the name of your Device Update instance?",
      "required": true
    },
    {
      "id": "adu_resultcode",
      "order": 5,
      "controlType": "textbox",
      "displayLabel": "What ResultCode are you encountering?",
      "required": true
    },
    {
      "id": "adu_ext_resultcode",
      "order": 6,
      "controlType": "textbox",
      "displayLabel": "What ExtendedResultCode are you encountering?",
      "required": true
    },
    {
      "id": "adu_importmanifest",
      "order": 8,
      "controlType": "textbox",
      "displayLabel": "Please upload the ADU Agent component logs from the device(s) encountering an issue.",
      "required": true
    },
    {
      "id": "problem_description",
      "order": 15,
      "controlType": "multilinetextbox",
      "displayLabel": "Description",
      "watermarkText": "Please provide additional information about your issue",
      "required": true,
      "useAsAdditionalDetails": true,
      "hints": [
        {
          "text": "Description of the issue and repro steps"
        }
      ]
    }
  ]
}
---