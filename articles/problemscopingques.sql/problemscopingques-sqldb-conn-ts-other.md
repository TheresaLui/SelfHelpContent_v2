<properties
	pageTitle="Other error not listed"
	description="Scoping questions to capture more details about errors encountered while connecting to SQL DB"
	authors="keithelm,vitomaz-msft"
	ms.author="keithelm,muruga,vitomaz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32745435"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="problemscopingques-sqldb-conn-ts-other"
	ownershipId="AzureData_AzureSQLDB_Connectivity"
/>
# Other error not listed
---
{
  "$schema": "SelfHelpContent",
  "resourceRequired": true,
  "subscriptionRequired": true,
  "title": "Other error not listed",
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
      "id": "sqlexception_received_on_client",
      "order": 2000,
      "controlType": "multilinetextbox",
      "displayLabel": "Paste detailed error message or stack trace. (Obscure the personally identifiable information).",
      "required": true,
      "watermarkText": "Always provide the full error text from the underlying client library (e.g., SqlClient), not the general error from your client application.  If available, include the client stack trace as well.",
      "diagnosticInputRequiredClients": "Portal"
    },
    {
      "id": "problem_description",
      "order": 1000,
      "controlType": "multilinetextbox",
      "displayLabel": "Please provide additional context for the error message you are encountering.",
      "required": true,
      "useAsAdditionalDetails": true
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
