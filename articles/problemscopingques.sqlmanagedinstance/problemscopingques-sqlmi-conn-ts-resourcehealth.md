<properties
	pageTitle="Resource Health Scoping Questions"
	description="Scoping questions to capture more details about Resource Health events"
	authors="vitomaz-msft,keithelm"
	ms.author="keithelm,vitomaz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32746128"
	productPesIds="16259"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="problemscopingques-sqlmi-conn-ts-resourcehealth"
	ownershipId="AzureData_AzureSQLMI"
/>
# Scoping questions for Resource Health events
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Resource Health scoping questions",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Diagnostics",
        "description": "Our diagnostics can identify the cause of many common service-related connection errors.",
        "insightNotAvailableText": "Our diagnostics did not detect any issues with your resource. See our recommended solutions below to troubleshoot your problem."
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
            "displayLabel": "When did the problem stop? (Up to 4 hours after problem start time)",
            "infoBalloonText": "Enter when the error stopped, or up to 4 hours after problem start time. Please run diagnostics with different time windows if the issue spans for more than 4 hours.",
            "required": false,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "new_or_recurring_issue",
            "order": 3,
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
            "watermarkText": ""
        },
        {
            "id": "sqlexception_received_on_client",
            "order": 2000,
            "controlType": "multilinetextbox",
            "displayLabel": "Paste detailed error message or stack trace. (Obscure the personally identifiable information).",
            "required": false,
            "visibility": true
        }
    ]
}
---
