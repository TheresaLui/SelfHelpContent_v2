<properties
	articleId="problemscopingques-exporting-metrics-or-querying-with-api-powershell-or-cli-log-analytics-storage-account-event-hub"
	pageTitle="Exporting metrics, or querying with API, PowerShell, or CLI - Log Analytics, Storage account, Event Hub"
	description="Exporting metrics, or querying with API, PowerShell, or CLI - Log Analytics, Storage account, Event Hub"
    authors="neilghuman"
	ms.author="neghuman"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32684752,32684753,32684751"
	productPesIds="16250"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	schemaVersion="1"
	ownershipId="AzureMonitoring_AzureMetrics"
/>

# Exporting metrics, or querying with API, PowerShell, or CLI - Log Analytics, Storage account, Event Hub"
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Exporting metrics, or querying with API, PowerShell, or CLI - Log Analytics, Storage account, Event Hub",
    "fileAttachmentHint": "If applicable, please upload a screenshot of the error.",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start happening?",
            "required": false
        },
        {
            "id": "problem_frequency",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "How frequently does the problem occur?",
            "watermarkText": "How frequently does the problem occur?",
            "required": true,
            "dropdownOptions": [
                {
                    "value": "Once",
                    "text": "Issue occurred once only"
                },
                {
                    "value": "Multiple",
                    "text": "Issue occurred more than once but not always"
                },
                {
                    "value": "Ongoing",
                    "text": "Issue occurs consistently"
                },
                {
                    "value": "dont_know_answer",
                    "text": "I don't know"
                }
            ]
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide the verbatim error message(s) you are receiving.",
            "watermarkText": "Provide the verbatim error message(s) you are receiving.",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Any verbatim error messages."
                },
                {
                    "text": "What is the source of the data?"
                },
                {
                    "text": "The timestamp and time zone of when the data was created."
                },
                {
                    "text": "The timestamp and time zone of when the data arrived at the destination."
                },
                {
                    "text": "Any unique details about the data such as a request id or other identifier."
                },
                {
                    "text": "If applicable, please attach a screenshot of the error."
                }
            ]
        },
        {
            "id": "additional_information",
            "order": 9,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional information about the issue.",
            "watermarkText": "Provide any additional information about the issue.",
            "required": false,
            "useAsAdditionalDetails": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---