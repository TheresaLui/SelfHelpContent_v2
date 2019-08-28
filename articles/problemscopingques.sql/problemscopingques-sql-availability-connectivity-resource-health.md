<properties
	pageTitle="Resource Health Scoping Questions"
	description="Scoping questions to capture more details about Availability and Connectivity\Resource Health support topic"
	authors="keithelm"
	ms.author="keithelm,muruga,emlisa"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630438"
	productPesIds="13491"
	cloudEnvironments="Public"
	schemaVersion="1"
	articleId="6B24CFBF-A6D2-4B0B-9A66-020664EF9408"
/>
# Error When Connecting to my Database
---
{
    "resourceRequired": false,
    "title": "Resource Health Scoping Questions",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "new_or_recurring_issue",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "How often does the issue ocur?",
            "watermarkText": "Choose an option",
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
            "infoBalloonText": "Please indicate what status Resource Health reports for your database or elastic pool",
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
                    "value": "Unknown",
                    "text": "Unknown/I don't know"
                }
            ],
            "required": true,
        },
        {
            "id": "problem_start_time",
            "order": 10,
            "controlType": "datetimepicker",
            "displayLabel": "Unavailability start time",
            "infoBalloonText": "Please provide the start time of the most recent occurence of the unavailability",
            "required": true,
        },
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional context for the error message you are encountering.",
            "required": true,
            "useAsAdditionalDetails": true,
            "watermarkText": "Always provide the full error text from the underlying client library (e.g., SqlClient), not the general error from your client application.  If available, include the client stack trace as well."
        }
    ],
    "$schema": "SelfHelpContent"
}
---
