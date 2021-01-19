<properties
	articleId="problemscopingques-sqlmi-monitor-errorlog"
	pageTitle="SQL Database Managed Instance"
	description="Scoping questions to get more details about errorlog issue"
	authors="vtpombei"
	authoralias="vtpombei"
	ms.author="vtpombei"
	selfHelpType="problemScopingQuestions"
	productPesIds="16259"
	supportTopicIds="32748864"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_AzureSQLMI"
/>
# SQL Database Managed Instance
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": true,
  "resourceRequired": false,
  "title": "ErrorLog",
  "fileAttachmentHint": "",
  "formElements": [
    {
      "id": "problem_start_time",
      "order": 1,
      "controlType": "datetimepicker",
      "displayLabel": "When did you face the issue?",
      "required": true
    },
    {
      "id": "type_issue",
      "order": 10,
      "controlType": "dropdown",
      "displayLabel": "What kind of issue are you facing",
      "watermarkText": "Choose an option",
			"dropdownOptions": [
                {
                    "value": "ingormation",
                    "text": "Information not available"
                },
                {
                    "value": "questions",
                    "text": "Questions or advisoring"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
    },
    {
      "id": "problem_description",
      "order": 99,
      "controlType": "multilinetextbox",
      "useAsAdditionalDetails": true,
      "displayLabel": "Details of the issue.",
      "watermarkText": "Please provide additional context for the error message you are encountering",
      "required": true
    }
  ]
}
---
