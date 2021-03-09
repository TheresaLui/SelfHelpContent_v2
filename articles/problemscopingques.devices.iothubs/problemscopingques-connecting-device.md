<properties
	pageTitle="Can't connect a device to IoT Hub"
	description="Can't connect device to IoT Hub for IoT Hub scoping questions"
	authors="camanle"
	ms.author="camanle"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630541"
	productPesIds="15946"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="problemscopoingques-connecting-device"
	ownershipId="AzureIot_IotHub"
/>
# Can't connect a device to IoT Hub
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": false,
  "resourceRequired": false,
  "title": "Can't connect a device to IoT Hub",
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
      "id": "feature",
      "order": 2,
      "controlType": "textbox",
      "displayLabel": "What feature are you having issue with?",
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
      "id": "documentation",
      "order": 10,
      "controlType": "textbox",
      "displayLabel": "Did you find any documentation related the problem? If so, please paste in the link",
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
      "order": 24,
      "visibility": "sdk_or_not == Yes",
      "controlType": "textbox",
      "displayLabel": "Version",
      "watermarkText": "Example: 1.21.0",
      "required": true
    },
    {
      "id": "service_sdk_or_not",
      "order": 30,
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
      "required": false
    },
    {
      "id": "service_sdk_language",
      "order": 35,
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
      "required": false
    },
    {
      "id": "service_sdk_version",
      "order": 40,
      "visibility": "service_sdk_or_not == Yes",
      "controlType": "textbox",
      "displayLabel": "Version",
      "watermarkText": "Example: 1.10.1",
      "required": false
    }
  ]
}
---