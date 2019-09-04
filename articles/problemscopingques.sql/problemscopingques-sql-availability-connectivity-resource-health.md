<properties
	pageTitle="Resource Health Scoping Questions"
	description="Scoping questions to capture more details about Availability and Connectivity\Resource Health support topic"
	authors="keithelm"
	ms.author="keithelm,muruga,emlisa"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630438"
	productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake"
	schemaVersion="1"
	articleId="6B24CFBF-A6D2-4B0B-9A66-020664EF9408"
/>
# Error When Connecting to my Database
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Resource Health Scoping Questions",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "Unavailability start time",
            "infoBalloonText": "Please provide the start time of the most recent occurence of unavailability.",
            "required": true
       },
        {
            "id": "new_or_recurring_issue",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "How often does the issue ocur?",
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
        }
    ]
}
---
