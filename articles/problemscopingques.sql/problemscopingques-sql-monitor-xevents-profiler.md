<properties
	articleId="problemscopingques-sql-monitor-xevents-profiler"
	pageTitle="Azure SQL Database"
	description="Scoping questions to get more details about extended events and sql profiler issue"
	authors="vtpombei"
	authoralias="vtpombei"
	ms.author="vtpombei"
	selfHelpType="problemScopingQuestions"
	productPesIds="13491"
	supportTopicIds="32749525"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_AzureSQLDB_Performance"
/>
# Azure SQL Database
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": true,
  "resourceRequired": false,
  "title": "Extended Events and SQL Profiler",
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
      "id": "xe_profiler",
      "order": 10,
      "controlType": "dropdown",
      "displayLabel": "Is the issue related to Extended Events or SQL Profiler?",
      "watermarkText": "Choose an option",
			"dropdownOptions": [
                {
                    "value": "xe",
                    "text": "Extended Events"
                },
                {
                    "value": "profiler",
                    "text": "SQL Profiler"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
    },
    {
      "id": "xe_type_issue",
      "order": 20,
      "visibility": "xe_profiler == xe || xe_profiler == dont_know_answer",
      "controlType": "dropdown",
      "displayLabel": "What kind of Extended Events issue are you facing",
      "watermarkText": "Choose an option",
			"dropdownOptions": [
                {
                    "value": "data",
                    "text": "Saving data from session"
                },
                {
                    "value": "capturing",
                    "text": "Not capturing events"
                },
                {
                    "value": "error",
                    "text": "Error creating session"
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
      "id": "profiler_type_issue",
      "order": 30,
      "visibility": "xe_profiler == profiler || xe_profiler == dont_know_answer",
      "controlType": "dropdown",
      "displayLabel": "What kind of SQL Profiler issue are you facing",
      "watermarkText": "Choose an option",
			"dropdownOptions": [
                {
                    "value": "connectivity",
                    "text": "Connectivity issues"
                },
                {
                    "value": "performance",
                    "text": " Performance impact"
                },
                {
                    "value": "event_target",
                    "text": "Event\target not available"
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
