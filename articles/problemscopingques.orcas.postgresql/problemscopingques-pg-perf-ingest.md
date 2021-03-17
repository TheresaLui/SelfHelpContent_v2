<properties
	pageTitle="Database Performance"
	description="Database Performance"
	authors="Joe Nelson"
	ms.author="jonels"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32731227"
	productPesIds="17068"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="problemscopingques-pg-perf-ingest"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
# Database Performance - Ingestion performance
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Database Query Performance - Ingestion performance",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Azure Database for PostgreSQL Perf Troubleshooter",
        "description": "Our Azure Database for PostgreSQL Perf Troubleshooter can help you troubleshoot and solve your problem.",
        "insightNotAvailableText": "Our troubleshooter did not detect any issues with your resource. Following the steps in Recommended Solution section below to troubleshoot your problem."
    },
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
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
            "id": "select_1",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the measured time when running 'SELECT 1' from your Postgres client?",
            "required": false
        },
        {
            "id": "client_location",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Is your client located in the same region as your database server?",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                }
            ],
            "required": false
        },
        {
            "id": "inserts_per_second",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Roughly how many rows per second are you seeing in your current ingestion?",
            "required": false
        },
        {
            "id": "insertion_method",
            "order": 6,
            "controlType": "dropdown",
            "displayLabel": "Which method do you use to ingest rows of data?",
            "dropdownOptions": [
                {
                    "value": "method_single",
                    "text": "One row per INSERT statement"
                },
                {
                    "value": "method_multi",
                    "text": "Multiple rows per INSERT statement"
                },
                {
                    "value": "method_copy",
                    "text": "The COPY or \\\\COPY command"
                },
                {
                    "value": "method_other",
                    "text": "Other"
                }
            ],
            "required": false
        },
        {
            "id": "insertion_connection",
            "order": 7,
            "controlType": "dropdown",
            "displayLabel": "Do you run INSERT statements in the same connection?",
            "dropdownOptions": [
                {
                    "value": "reused_connection",
                    "text": "All INSERT statements use the same connection per thread/process"
                },
                {
                    "value": "split_connection",
                    "text": "Connections are closed and reestablished between INSERT statements"
                },
                {
                    "value": "na_connection",
                    "text": "Not applicable (another method)"
                }
            ],
            "required": false
        },
        {
            "id": "multithreaded",
            "order": 8,
            "controlType": "dropdown",
            "displayLabel": "Do you ingest from multiple processes or threads at once from the source?",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 9,
            "controlType": "multilinetextbox",
            "displayLabel": "Problem description",
            "watermarkText": "Extra notes about your data ingestion.",
            "required": true,
            "diagnosticInputRequiredClients": "Portal",
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
