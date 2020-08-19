<properties
	pageTitle="Scoping questions for Firewall rules and related issues"
	description="Scoping questions to capture more details about firewall configuration issue."
	authors="keithelm"
	ms.author="keithelm,muruga,emlisa,swbharti,vimahadi"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32745429,32745431"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="1BBD6149-205A-42C1-A193-7B2C571FFFA6-new-st"
	ownershipId="AzureData_AzureSQLDB_Availability"
/>
# Scoping questions for Firewall Errors
---
{
  "$schema": "SelfHelpContent",
  "resourceRequired": true,
  "subscriptionRequired": true,
  "title": "Firewall errors related scoping questions",
  "fileAttachmentHint": "",
	"diagnosticCard": {
	  "title": "Scoping questions for Firewall rules and related issues",
	  "description": "These diagnostics will check for errors with the Database Firewall Rules",
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
      "id": "problem_description",
      "order": 2,
      "controlType": "multilinetextbox",
      "displayLabel": "Additional context to help us solve your issue.",
      "required": true,
      "useAsAdditionalDetails": true,
      "watermarkText": "On the Basics tab, please ensure you selected a server, database or elastic pool in the Resource dropdown so we know what resource you need assistance with.  Add any additional details that may help us troubleshoot your issue."
    },
		{
      "id": "client_address",
      "order": 10,
      "controlType": "textbox",
      "displayLabel": "Your Client IP Address",
      "watermarkText": "Enter the public IP address. Ex. 167.2.2.2",
      "required": true,
      "useAsAdditionalDetails": true,
      "diagnosticInputRequiredClients": "Portal, ASC"
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
