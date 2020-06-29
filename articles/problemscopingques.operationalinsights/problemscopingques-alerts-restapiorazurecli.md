
<properties
pageTitle="REST API or Azure Command Line Interface (CLI)"
description="REST API or Azure Command Line Interface (CLI)"
articleId="problemscopingques-REST_API_or_Azure_Command_Line_Interface_CLI"
authors="yossiy"
ms.author="yossiy"
selfHelpType="problemScopingQuestions"
supportTopicIds="32633014"
productPesIds="15725"
cloudEnvironments="Public, Fairfax, usnat, ussec"
schemaVersion="1"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# REST API or Azure Command Line Interface (CLI)
 
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "REST API or Azure Command Line Interface (CLI)",
    "fileAttachmentHint": "Provide screenshot of alert rule configuration with query and error message you are receiving",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "interface_type",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Which interface has this problem?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "REST",
                    "text": "REST"
                },
                {
                    "value": "CLI",
                    "text": "CLI"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Not sure"
                }
            ],
            "required": true
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "hints": []
        }
    ],
    "$schema": "SelfHelpContent"
}
---