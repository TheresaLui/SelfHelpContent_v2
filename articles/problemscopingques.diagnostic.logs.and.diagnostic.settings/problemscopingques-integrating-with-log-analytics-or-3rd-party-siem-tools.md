<properties
	articleId="problemscopingques-integrating-with-log-analytics-or-3rd-party-siem-tools"
	pageTitle="Integrating with Log Analytics or 3rd party SIEM tools"
	description="Integrating with Log Analytics or 3rd party SIEM tools"
    authors="neilghuman"
	ms.author="neghuman"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32684712,32684711"
	productPesIds="16875"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	schemaVersion="1"
	ownershipId="AzureMonitoring_DiagnosticLogsandSettings"
/>

# Integrating with Log Analytics or 3rd party SIEM tools"
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Integrating with Log Analytics or 3rd party SIEM tools",
    "fileAttachmentHint": "If possible, please upload a screenshot.",
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
            "order": 3,
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
                    "text": "Issue occurs for every alert instance"
                },
                {
                    "value": "dont_know_answer",
                    "text": "I don't know"
                }
            ]
        },
                {
            "id": "log_destination",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "What is the diagnostic log destination that is experiencing the issue?",
            "watermarkText": "What is the diagnostic log destination that is experiencing the issue?",
            "required": true,
            "dropdownOptions": [
                {
                    "value": "Event Hub",
                    "text": "Event Hug"
                },
                {
                    "value": "Log Analytics",
                    "text": "Log Analytics"
                },
                {
                    "value": "Storage",
                    "text": "Storage"
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
            "displayLabel": "Provide a description of the problem.",
            "watermarkText": "Provide a description of the problem.",
            "required": true,
            "hints": []
        },
        {
            "id": "additional_information",
            "order": 9,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional information about the issue.",
            "watermarkText": "Provide any additional information about the issue.",
            "required": false,
            "useAsAdditionalDetails": true
         }
    ],
    "$schema": "SelfHelpContent"
}
---