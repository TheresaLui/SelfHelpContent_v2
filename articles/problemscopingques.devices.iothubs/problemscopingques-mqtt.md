<properties
	pageTitle="3rd party MQTT client"
	description="3rd party MQTT client for IoT Hub scoping questions"
	authors="jlian"
	ms.author="jlian"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630540"
	productPesIds="15946"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="87cabeeb-a572-421d-bc71-5ba6a30a72b4"
	ownershipId="AzureIot_IotHub"
/>
# 3rd party MQTT client
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": false,
  "resourceRequired": false,
  "title": "3rd party MQTT client",
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
      "order": 5,
      "controlType": "textbox",
      "displayLabel": "What 3rd party MQTT client are you using?",
      "watermarkText": "Example: paho-mqtt",
      "required": false
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