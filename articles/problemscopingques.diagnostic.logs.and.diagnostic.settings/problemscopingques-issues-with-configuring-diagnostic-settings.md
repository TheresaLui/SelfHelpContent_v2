<properties
	articleId="problemscopingques-issues-with-configuring-diagnostic-settings"
	pageTitle="Issues with configuring diagnostic settings"
	description="Issues with configuring diagnostic settings"
    authors="neilghuman"
	ms.author="neghuman"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32684710,32684709,32684708,32684707,32684706,32684705,32684704,32684703"
	productPesIds="16875"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	schemaVersion="1"
	ownershipId="AzureMonitoring_DiagnosticLogsandSettings"
/>

# Issues with configuring diagnostic settings"
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Issues with configuring diagnostic settings",
    "fileAttachmentHint": "If possible, please upload a screenshot of the error.",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start happening?",
            "required": false
        },
                {
            "id": "interface",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Which user experience are you using?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Azure portal",
                    "text": "Azure portal"
                },
                {
                    "value": "Azure PowerShell",
                    "text": "Azure PowerShell"
                },
                {
                    "value": "Azure CLI",
                    "text": "Azure CLI"
                },
                {
                    "value": "Azure REST API",
                    "text": "Azure REST API"
                },
                {
                    "value": "Azure Resource Manager (ARM) template",
                    "text": "Azure Resource Manager (ARM) template"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other"
                }
            ],
            "required": true
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide the verbatim error message(s) you are receiving.",
            "watermarkText": "Provide the verbatim error message(s) you are receiving.",
            "required": true,
            "hints": [
                {
                    "text": "If possible, please attach a screenshot of the error within the File upload section below. "
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