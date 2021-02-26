<properties
	pageTitle="Device Update for Azure IoT Hub resource issues"
	description="Scoping questions for Device Update for Azure IoT Hub resource issues"
	authors="chrisjlin"
	ms.author="lichris"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32787855"
	productPesIds="17393"
  articleId="problemscopingques-resource"
	cloudEnvironments="public"
	schemaVersion="1"
	ownershipId="EDS_AzureDeviceUpdate"
/>
# Device Update for Azure IoT Hub resource issues
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": false,
  "resourceRequired": false,
  "title": "Issues with Device Update resource",
  "fileAttachmentHint": "Please upload the following if available: screenshots of errors.",
  "formElements": [
    {
      "id": "problem_start_time",
      "order": 1,
      "controlType": "datetimepicker",
      "displayLabel": "When did the problem start?",
      "required": true
    },
    {
      "id": "iot_hub_name",
      "order": 2,
      "controlType": "textbox",
      "displayLabel": "What is the name of your IoT Hub instance?",
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
        }
      ]
    }
  ]
}
---
