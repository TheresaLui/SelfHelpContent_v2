<properties
	pageTitle="Login failed"
	description="Scoping questions to capture more details about failed logins"
	authors="vitomaz"
	ms.author="keithelm, muruga, vitomaz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32745428,32745433"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="problemscopingques-sql-conn-ts-18456"
	ownershipId="AzureData_AzureSQLDB_Connectivity"
/>
# Login failed
---
{
  "$schema": "SelfHelpContent",
  "resourceRequired": true,
  "subscriptionRequired": true,
  "title": "Failed Login",
  "fileAttachmentHint": "",
  "diagnosticCard": {
    "title": "Failed Login Troubleshooter",
    "description": "The Failed Login Troubleshooter can identify the cause of many common failed login errors.",
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
      "id": "auth_method",
      "order": 3,
      "controlType": "dropdown",
      "displayLabel": "What authentication method you are using?",
      "required": true,
      "watermarkText": "Authentication method",
      "infoBalloonText": "Choose the authentication method you are using",
      "dropdownOptions": [
        {
          "text": "SQL Server Authentication",
          "value": "SQL"
        },
        {
          "text": "Application token authentication",
          "value": "Token"
        },
        {
          "text": "Azure Active Directory Password",
          "value": "AADPassword"
        },
        {
          "text": "Azure Active Directory Integrated",
          "value": "AADIntegrated"
        },
        {
          "text": "Azure Active Directory Universal with Multi-Factor Authentication",
          "value": "AADUniversalMFA"
        },
        {
          "text": "Don't know or not applicable",
          "value": "dont_know_answer"
        }
      ],
      "dynamicDropdownOptions": null,
      "diagnosticInputRequiredClients": "Portal"
    },
    {
      "id": "problem_description",
      "order": 1000,
      "controlType": "multilinetextbox",
      "displayLabel": "Always provide the full error text from the underlying client library (e.g., SqlClient), not the general error from your client application.  If available, include the client stack trace as well.",
      "required": true,
      "useAsAdditionalDetails": true
    }
  ]
}
---
