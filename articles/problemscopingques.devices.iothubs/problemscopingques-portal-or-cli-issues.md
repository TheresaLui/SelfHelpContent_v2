<properties
	pageTitle="Issue with IoT Portal or CLI commands"
	description="Azure Portal or CLI issues for IoT Hub scoping questions"
	authors="camanle"
	ms.author="camanle"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630526"
	productPesIds="15946"
	cloudEnvironments="public,BlackForest,Fairfax,Mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="problemscopingques-portal-or-cli-issues"
	ownershipId="AzureIot_IotHub"
/>
# Issue with IoT Portal or CLI commands
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": false,
  "resourceRequired": false,
  "title": "Issue with IoT Portal or CLI commands",
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
      "id": "feature_issues",
      "order": 10,
      "controlType": "textbox",
      "displayLabel": "Which feature are you having issues with?",
      "watermarkText": "Example: Networking, Certificates, IoT Devices, etc",
      "required": false
    },
    {
      "id": "cli",
      "order": 20,
      "controlType": "textbox",
      "displayLabel": "If you are using CLI, which command are you having issue with?",
      "watermarkText": "For a list of commands, please see this page - https://docs.microsoft.com/cli/azure/ext/azure-cli-iot-ext/iot/hub?view=azure-cli-latest",
      "required": false
    }
  ]
}
---