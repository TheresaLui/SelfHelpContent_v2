<properties
	pageTitle="Issues with IoT devices"
	description="Issues with IoT devices for IoT Hub scoping questions"
	authors="jlian"
	ms.author="jlian"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630568,32630545,32630546, 32783516"
	productPesIds="15946"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="f843dcf7-98d9-4cb4-9c7f-d34cb5ab74ed"
	ownershipId="AzureIot_IotHub"
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
      "required": true
    },
    {
      "id": "device_id",
      "order": 2,
      "controlType": "textbox",
      "displayLabel": "Affected device IDs",
      "infoBalloonText": "Ideally 3 devices",
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
    },
    {
      "id": "protocol",
      "order": 10,
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
      "order": 15,
      "controlType": "dropdown",
      "infoBalloonText": "IoT Hub Device SDKs enable you to build apps that run on your IoT devices using device client or module client. These apps send telemetry to your IoT hub, and optionally receive messages, job, method, or twin updates from your IoT hub. To learn more, see <a href='https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-sdks'>Understand and use Azure IoT Hub SDKs</a> ",
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
      "order": 20,
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
        },
        {
          "value": "dont_know_answer",
          "text": "Don't know"
        }
      ],
      "required": true
    },
    {
      "id": "sdk_version",
      "order": 25,
      "visibility": "sdk_or_not == Yes",
      "controlType": "textbox",
      "displayLabel": "Version",
      "watermarkText": "Example: 1.21.0",
      "required": true
    }
  ]
}
---