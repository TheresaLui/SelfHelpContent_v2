<properties
	pageTitle="Scoping Questions for Azure Active Directory (AAD) authentication"
	description="Scoping questions to capture more details about Azure Active Directory (AAD) authentication issue."
	authors="keithelm"
	ms.author="keithelm,muruga,emlisa,swbhartims,vimahadi,subbuk"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630414, 32630460"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake"
	schemaVersion="1"
	articleId="217152B3-3A59-4441-8B67-B20B2DE5CD95"
/>

# Scoping questions for Configure or use Azure Active Directory (AAD) authentication
---
{
  "$schema": "SelfHelpContent",
  "resourceRequired": true,
  "subscriptionRequired": true,
  "title": "Azure Active Directory (AAD) authentication scoping questions",
  "fileAttachmentHint": "",
  "diagnosticCard": {
    "title": "Azure Active Directory (AAD) authentication scoping questions",
    "description": "Below diagnostics will check for errors occurred while configuring or using Azure Active Directory (AAD) authentication. Provide additional details for the problem that you are experiencing.",
		"description": "",
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
			"id": "aad_issue_type",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "Choose an option that best describes your AAD issue.",
			"required": true,
			"infoBalloonText": "AAD Issue category",
			"diagnosticInputRequiredClients": "Portal, ASC",
			"dropdownOptions": [
					{
							"text": "Logging using AAD",
							"value": "AADLogin"
					},
					{
							"text": "Creating new AAD Users",
							"value": "AADCreateUser"
					},
					{
							"text": "Setting up AAD administrator",
							"value": "AADSetupAdmin"
					},
					{
							"text": "Other AAD issues",
							"value": "AADOthers"
					}
			],
			"dynamicDropdownOptions": null,
			"diagnosticInputRequiredClients": "Portal"
		},
    {
      "id": "sqlexception_received_on_client",
      "order": 4,
      "controlType": "multilinetextbox",
      "displayLabel": "Paste detailed error message or stack trace. (Obscure the personally identifiable information).",
      "required": false,
      "visibility": "aad_issue_type == AADLogin || aad_issue_type == AADCreateUser || aad_issue_type == AADOthers",
      "diagnosticInputRequiredClients": "Portal"
    },
    {
      "id": "database_name",
      "order": 5,
      "controlType": "dropdown",
      "displayLabel": "If you are creating this support request from the SQL Server (and not from a database), choose the impacted database. Note: The dropdown will state 'Response not found' if you are creating this support request from database.",
      "required": false,
      "infoBalloonText": "Which of these databases are you filing a support ticket for?",
      "diagnosticInputRequiredClients": "Portal, ASC",
      "dynamicDropdownOptions": {
        "uri": "{resourceId}/databases?api-version=2017-10-01-preview",
        "jTokenPath": "value",
        "textProperty": "name",
        "valueProperty": "id",
        "textPropertyRegex": null,
        "defaultDropdownOptions": {
          "value": "dont_know_answer",
          "text": "Don't know / None of these"
        }
      }
    }
  ]
}
---
