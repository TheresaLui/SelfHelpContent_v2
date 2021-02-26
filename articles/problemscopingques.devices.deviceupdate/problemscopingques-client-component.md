<properties
	pageTitle="Device Update for Azure IoT Hub ADU client component issues"
	description="Scoping questions for Device Update for Azure IoT Hub ADU client component issues"
	authors="chrisjlin"
	ms.author="lichris"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32787856"
	productPesIds="17393"
  articleId="problemscopingques-client-component"
	cloudEnvironments="public"
	schemaVersion="1"
	ownershipId="EDS_AzureDeviceUpdate"
/>
# Device Update for Azure IoT Hub ADU client component issues
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": false,
  "resourceRequired": false,
  "title": "Issues with Device Update client components",
  "fileAttachmentHint": "Please upload the following if available: ADU Agent logs, DO Agent logs, Device Update configuration file.",
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
      "id": "adu_deviceid",
      "order": 7,
      "controlType": "textbox",
      "displayLabel": "What is the Device ID of the device encountering an issue?",
      "required": false
    },
    {
      "id": "adu_agenttype",
      "order": 10,
      "controlType": "textbox",
      "displayLabel": "What type of ADU Agent is running on the device encountering an issue? (for example, Azure Percept, Edge Gateway, Other)",
      "required": false
    },
    {
      "id": "adu_ostype",
      "order": 11,
      "controlType": "textbox",
      "displayLabel": "What type of Operating System is running on the device encountering an issue?",
      "required": false
    },
    {
      "id": "adu_devicearch",
      "order": 12,
      "controlType": "textbox",
      "displayLabel": "What architecture is being used by the device encountering an issue?",
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
