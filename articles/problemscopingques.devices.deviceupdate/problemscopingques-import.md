<properties
	pageTitle="Device Update for Azure IoT Hub import issues"
	description="Scoping questions for Device Update for Azure IoT Hub import issues"
	authors="chrisjlin"
	ms.author="lichris"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32787860, 32787862"
	productPesIds="17393"
  articleId="problemscopingques-import"
	cloudEnvironments="public, fairfax, usnat, ussec"
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
      "required": false
    },
    {
      "id": "adu_account_name",
      "order": 3,
      "controlType": "textbox",
      "displayLabel": "What is the name of your Device Update account?",
      "required": false
    },
    {
      "id": "adu_instance_name",
      "order": 4,
      "controlType": "textbox",
      "displayLabel": "What is the name of your Device Update instance?",
      "required": false
    },
    {
      "id": "adu_resultcode",
      "order": 5,
      "controlType": "textbox",
      "displayLabel": "What ResultCode are you encountering?",
      "required": false
    },
    {
      "id": "adu_ext_resultcode",
      "order": 6,
      "controlType": "textbox",
      "displayLabel": "What ExtendedResultCode are you encountering?",
      "required": false
    },
    {
      "id": "problem_description",
      "order": 15,
      "controlType": "multilinetextbox",
      "displayLabel": "Description",
      "watermarkText": "Provide additional information about your issue",
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
