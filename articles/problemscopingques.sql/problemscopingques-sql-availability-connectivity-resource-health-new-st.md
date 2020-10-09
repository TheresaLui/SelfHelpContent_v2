<properties
	pageTitle="Resource Health Scoping Questions"
	description="Scoping questions to capture more details about the resource health issue."
	authors="keithelm"
	ms.author="keithelm,muruga,emlisa,swbharti,vimahadi"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32745438"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="6B24CFBF-A6D2-4B0B-9A66-020664EF9408-new-st"
	ownershipId="AzureData_AzureSQLDB_Availability"
/>
# Scoping questions for My database was reported as unavailable (Resource Health)
---
{
  "$schema": "SelfHelpContent",
  "resourceRequired": true,
  "subscriptionRequired": true,
  "title": "Resource Health scoping questions",
  "fileAttachmentHint": "",
	"diagnosticCard": {
	  "title": "Resource Health scoping questions",
	  "description": "These diagnostics will check for errors and issues with Resource Health",
	  "insightNotAvailableText": "We did not find any issues."
	},
  "formElements": [
    {
      "id": "problem_start_time",
      "order": 1,
      "controlType": "datetimepicker",
      "displayLabel": "Unavailability start time",
      "infoBalloonText": "Please provide the start time of the most recent occurrence of unavailability.",
      "required": true
    },
    {
      "id": "new_or_recurring_issue",
      "order": 2,
      "controlType": "dropdown",
      "displayLabel": "How often does the issue occur?",
      "watermarkText": "Choose an option",
      "infoBalloonText": "Is the unavailability recurring or a one time issue?",
      "dropdownOptions": [
        {
          "value": "one_time",
          "text": "One time"
        },
        {
          "value": "recurring_issue",
          "text": "Recurring issue"
        }
      ],
      "required": false
    },
    {
      "id": "reported_resource_status",
      "order": 5,
      "controlType": "dropdown",
      "displayLabel": "What status does Resource Health report?",
      "watermarkText": "Choose an option",
      "infoBalloonText": "Please indicate what status Resource Health reports for your database or elastic pool.",
      "dropdownOptions": [
        {
          "value": "Available",
          "text": "Available"
        },
        {
          "value": "Degraded",
          "text": "Degraded"
        },
        {
          "value": "Unavailable",
          "text": "Unavailable"
        },
        {
          "value": "dont_know_answer",
          "text": "Unknown/I don't know"
        }
      ],
      "required": false
    },
    {
      "id": "problem_description",
      "order": 1000,
      "controlType": "multilinetextbox",
      "displayLabel": "Additional context to help us solve your issue.",
      "required": true,
      "useAsAdditionalDetails": true,
      "watermarkText": "On the Basics tab, please ensure you selected a server, database or elastic pool in the Resource dropdown so we know what resource you need assistance with.  Add any additional details that may help us troubleshoot your issue."
    },
    {
      "id": "sqlexception_received_on_client",
      "order": 2000,
      "controlType": "multilinetextbox",
      "displayLabel": "Paste detailed error message or stack trace. (Obscure the personally identifiable information).",
      "required": false,
      "visibility": true,
      "diagnosticInputRequiredClients": "Portal"
    },
    {
      "id": "database_name",
      "order": 3000,
      "controlType": "dropdown",
      "displayLabel": "Please provide the database name for which you are creating a support ticket. If multiple databases are affected, select one of the affected databases to start an investigation",
      "required": false,
      "infoBalloonText": "Which of these databases are you filing a ticket for?",
			"diagnosticInputRequiredClients": "Portal, ASC",
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
