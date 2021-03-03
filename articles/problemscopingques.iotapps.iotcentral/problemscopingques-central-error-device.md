<properties
	pageTitle="Issues with IoT Central devices"
	description="Issues with IoT Central devices for IoT Central scoping questions"
	authors="jajens"
	ms.author="jajens"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32727889,32592868"
	productPesIds="16284"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake,usnat,ussec"
	schemaVersion="1"
	articleId="ed4e0c35-4a9e-4d6b-a384-ffda98ea2fe5"
	ownershipId="AzureIot_IotCentral"
/>
# Issues with IoT Central devices
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": false,
  "resourceRequired": false,
  "title": "Issues with IoT Central devices",
  "fileAttachmentHint": "Upload logs or screenshots of errors if available",
  "formElements": [
    {
      "id": "problem_start_time",
      "order": 1,
      "controlType": "datetimepicker",
      "displayLabel": "When did the problem start?",
      "required": true
    },
	    {
      "id": "device_id",
      "order": 2,
      "controlType": "textbox",
      "displayLabel": "Affected device IDs",
      "watermarkText": "Example: myEdgeDevice, chiller-02",
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
        },
        {
          "text": "Error logs with timestamp (indicate timezone or UTC)"
        }
      ]
    }
  ]
}
---