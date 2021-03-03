<properties
	pageTitle="Device Update for Azure IoT Hub deployment issues"
	description="Scoping questions for Device Update for Azure IoT Hub deployment issues"
	authors="chrisjlin"
	ms.author="lichris"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32787857, 32787858, 32787864, 32787865"
	productPesIds="17393"
  articleId="problemscopingques-deployment"
	cloudEnvironments="public"
	schemaVersion="1"
	ownershipId="EDS_AzureDeviceUpdate"
/>
# Device Update for Azure IoT Hub deployment issues
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": false,
  "resourceRequired": false,
  "title": "Issues with Device Update client components",
  "fileAttachmentHint": "Please upload the following if available: ADU Agent logs, DO Agent logs, Device Update configuration file, import manifest.",
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
      "id": "adu_deploymentid",
      "order": 3,
      "controlType": "textbox",
      "displayLabel": "What is the Deployment ID for the deployment encountering an issue?",
      "required": false
    },
    {
      "id": "adu_updateid",
      "order": 4,
      "controlType": "textbox",
      "displayLabel": "What is the Update ID for the update content encountering an issue?",
      "required": false
    },
    {
      "id": "iot_hub_name",
      "order": 5,
      "controlType": "textbox",
      "displayLabel": "What is the name of your IoT Hub instance?",
      "required": false
    },
    {
      "id": "adu_account_name",
      "order": 6,
      "controlType": "textbox",
      "displayLabel": "What is the name of your Device Update account?",
      "required": false
    },
    {
      "id": "adu_instance_name",
      "order": 7,
      "controlType": "textbox",
      "displayLabel": "What is the name of your Device Update instance?",
      "required": false
    },
    {
      "id": "adu_resultcode",
      "order": 8,
      "controlType": "textbox",
      "displayLabel": "What ResultCode are you encountering?",
      "required": false
    },
    {
      "id": "adu_ext_resultcode",
      "order": 9,
      "controlType": "textbox",
      "displayLabel": "What ExtendedResultCode are you encountering?",
      "required": false
    },
    {
      "id": "adu_deviceid",
      "order": 10,
      "controlType": "textbox",
      "displayLabel": "What is the Device ID of the device encountering an issue?",
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
