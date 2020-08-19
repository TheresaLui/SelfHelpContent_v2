<properties
	pageTitle="Dropped connections"
	description="Scoping questions to capture more details about dropped connections"
	authors="keithelm"
	ms.author="keithelm,muruga"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="332745426"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="4C560386-D637-4B09-A75B-FFC643DB8430"
	ownershipId="AzureData_AzureSQLDB_Availability"
/>
# Error When Connecting to my Database
---
{
  "$schema": "SelfHelpContent",
  "resourceRequired": true,
  "subscriptionRequired": true,
  "title": "Dropped connections",
  "fileAttachmentHint": "",
  "diagnosticCard": {
    "title": "SQL DB Connectivity Troubleshooter",
    "description": "Our SQL DB Connectivity Troubleshooter can help you troubleshoot and solve your problem.",
    "insightNotAvailableText": "Our troubleshooter did not detect any issues with your resource. See our manual troubleshooting steps below to troubleshoot your problem."
  },
  "formElements": [
    {
      "id": "problem_start_time",
      "order": 1,
      "controlType": "datetimepicker",
      "displayLabel": "When did the problem start?",
      "infoBalloonText": "Enter the approximate time you started to see the error.",
      "required": true,
      "diagnosticInputRequiredClients": "Portal"
    },
    {
      "id": "problem_end_time",
      "order": 2,
      "controlType": "datetimepicker",
      "displayLabel": "When did the problem stop? (If ongoing, leave this field blank)",
      "infoBalloonText": "Enter when the error stopped, or leave blank if the issue is ongoing.",
      "required": false,
      "diagnosticInputRequiredClients": "Portal"
    },
    {
      "id": "connecting_from",
      "order": 5,
      "controlType": "dropdown",
      "displayLabel": "Where is your client application running?",
      "watermarkText": "Choose an option",
      "infoBalloonText": "Knowing where your client application is connecting from may help us troubleshoot the issue further.",
      "dropdownOptions": [
        {
          "value": "within_azure",
          "text": "Within Azure"
        },
        {
          "value": "on_premise",
          "text": "On-premise network"
        },
        {
          "value": "other_cloud",
          "text": "Other cloud service provider"
        },
        {
          "value": "other_hoster",
          "text": "Other application hoster/ISP"
        },
        {
          "value": "dont_know_answer",
          "text": "I don't know"
        }
      ],
      "required": true,
      "diagnosticInputRequiredClients": "Portal"
    },
    {
      "id": "problem_description",
      "order": 1000,
      "controlType": "multilinetextbox",
      "displayLabel": "Please provide additional context for the error message you are encountering.",
      "required": true,
      "useAsAdditionalDetails": true,
      "watermarkText": "Always provide the full error text from the underlying client library (e.g., SqlClient), not the general error from your client application.  If available, include the client stack trace as well."
    },
    {
      "id": "database_name",
      "order": 3000,
      "controlType": "dropdown",
      "displayLabel": "Please provide the database name for which you are creating a support ticket. If multiple databases are affected, select one of the affected databases to start an investigation",
      "required": false,
      "infoBalloonText": "Which of these databases are you filing a ticket for?",
      "dynamicDropdownOptions": {
        "uri": "{resourceId}/databases?api-version=2017-10-01-preview",
        "jTokenPath": "value",
        "textProperty": "name",
        "valueProperty": "id",
        "textPropertyRegex": null,
        "defaultDropdownOptions": {
          "value": "dont_know_answer",
          "text": "Don't know/None of these"
        }
      }
    }
  ]
}
---
