<properties
	pageTitle="Can't reach device from IoT Hub"
	description="Can't reach device from IoT Hub for IoT Hub scoping questions"
	authors="jlian"
	ms.author="jlian"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630539,32630547"
	productPesIds="15946"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake"
	schemaVersion="1"
	articleId="f843dcf7-98d9-4cb4-9c7f-d34cb5ab74ed"
/>
# Can't reach device from IoT Hub
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": false,
  "resourceRequired": false,
  "title": "Can't reach device from IoT Hub",
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
      "order": 5,
      "visibility": "sdk_or_not == Yes",
      "controlType": "textbox",
      "displayLabel": "Version",
      "watermarkText": "Example: 1.21.0",
      "required": true
    },
    {
      "id": "service_sdk_or_not",
      "order": 6,
      "controlType": "dropdown",
      "infoBalloonText": "IoT Hub Service SDKs enable you to build backend applications to manage your IoT hub, and optionally send messages, schedule jobs, invoke direct methods, or send desired property updates to your IoT devices or modules. To learn more, see <a href='https://docs.microsoft.com/azure/iot-hub/iot-hub-devguide-sdks'>Understand and use Azure IoT Hub SDKs</a> ",
      "displayLabel": "Are you using the IoT Hub Service SDK to send direct method or cloud-to-device messages?",
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
      "id": "service_sdk_language",
      "order": 7,
      "visibility": "service_sdk_or_not == Yes",
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
      "order": 8,
      "visibility": "service_sdk_or_not == Yes",
      "controlType": "textbox",
      "displayLabel": "Version",
      "watermarkText": "Example: 1.10.1",
      "required": true
    },
    {
      "id": "problem_description",
      "order": 9,
      "controlType": "multilinetextbox",
      "displayLabel": "Details, error logs, and affected device IDs",
      "watermarkText": "Provide additional information, logs, and device IDs.",
      "required": true,
      "useAsAdditionalDetails": true,
      "hints": [
        {
          "text": "Examples of device IDs (ideally 3)"
        },
        {
          "text": "Error logs with timestamp (indicate timezone or UTC)"
        },
        {
          "text": "Any other details"
        }
      ]
    }
  ]
}
---