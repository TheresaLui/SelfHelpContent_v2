<properties
	articleId="problemscopingques-diagnostic-logs-are-missing-or-delayed"
	pageTitle="Diagnostic logs are missing or delayed"
	description="Diagnostic logs are missing or delayed"
    authors="neilghuman"
	ms.author="neghuman"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32684720,32684719,32684718,32684717,32684716,32684715,32684714,32684713"
	productPesIds="16875"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	schemaVersion="1"
	ownershipId="AzureMonitoring_DiagnosticLogsandSettings"
/>

# Diagnostic logs are missing or delayed"
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Diagnostic logs are missing or delayed",
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
            "displayLabel": "Provide details of the data that is either missing or delayed.",
            "watermarkText": "Provide details of the data that is either missing or delayed.",
            "required": true,
            "hints": [
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
            "useAsAdditionalDetails": true
         }
    ],
    "$schema": "SelfHelpContent"
}
---