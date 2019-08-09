<properties
	pageTitle="Issues with IoT devices"
	description="Issues with IoT devices for IoT Hub scoping questions"
	authors="jlian"
	ms.author="jlian"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630568"
	productPesIds="15946"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake"
	schemaVersion="1"
	articleId="f843dcf7-98d9-4cb4-9c7f-d34cb5ab74ed"
/>
# Issues with IoT devices
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": false,
  "resourceRequired": false,
  "title": "Issues with IoT devices",
  "fileAttachmentHint": "Upload screenshots of errors if available",
  "formElements": [
    {
      "id": "problem_start_time",
      "order": 1,
      "controlType": "datetimepicker",
      "displayLabel": "When did the problem start?",
      "required": false
    },
    {
      "id": "protocol",
      "order": 2,
      "controlType": "dropdown",
      "infoBalloonText": "IoT Hub supports MQTT, AMQP, and HTTPS protocols. To learn more, see <a href='https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-protocols'>Choose a communication protocol</a> ",
      "displayLabel": "What protocol are you using?",
      "watermarkText": "Choose an option",
      "dropdownOptions": [
        {
          "value": "MQTT",
          "text": "MQTT"
        },
        {
          "value": "AMQP",
          "text": "AMQP"
        },
        {
          "value": "HTTPS",
          "text": "HTTPS"
        },
        {
          "value": "dont_know_answer",
          "text": "Don't know"
        }
      ],
      "required": true
    },
    {
      "id": "sdk_or_not",
      "order": 3,
      "controlType": "dropdown",
      "infoBalloonText": "To learn more about the Azure IoT Device SDKs, see <a href='https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-sdks'>Understand and use Azure IoT Hub SDKs</a> ",
      "displayLabel": "Are you using Azure IoT Device SDKs?",
      "watermarkText": "Choose an option",
      "dropdownOptions": [
        {
          "value": "Yes",
          "text": "Yes"
        },
        {
          "value": "No",
          "text": "No"
        },
        {
          "value": "dont_know_answer",
          "text": "Don't know"
        }
      ],
      "required": true
    },
    {
      "id": "sdk_language",
      "order": 4,
      "visibility": "sdk_or_not == Yes",
      "controlType": "dropdown",
      "displayLabel": "Language",
      "watermarkText": "Choose an option",
      "dropdownOptions": [
        {
          "value": "C# (.NET)",
          "text": "C# (.NET)"
        },
        {
          "value": "C",
          "text": "C"
        },
        {
          "value": "Java",
          "text": "Java"
        },
        {
          "value": "Node.JS",
          "text": "Node.JS"
        },
        {
          "value": "Python",
          "text": "Python"
        },
        {
          "value": "iOS",
          "text": "iOS"
        }
      ],
      "required": false
    },
    {
      "id": "sdk_version",
      "order": 5,
      "visibility": "sdk_or_not == Yes",
      "controlType": "textbox",
      "displayLabel": "Version",
      "watermarkText": "Example: 1.21.0",
      "required": false
    },
    {
      "id": "problem_description",
      "order": 6,
      "controlType": "multilinetextbox",
      "displayLabel": "Details, error logs, and affected device IDs",
      "watermarkText": "Provide additional information, logs, and device IDs.",
      "required": true,
      "useAsAdditionalDetails": true,
      "hints": [
        {
          "text": "Device logs of errors with latest timestamp (indicate timezone or UTC)"
        },
        {
          "text": "Examples of device IDs (ideally 3)"
        },
        {
          "text": "Any other details"
        }
      ]
    }
  ]
}
---