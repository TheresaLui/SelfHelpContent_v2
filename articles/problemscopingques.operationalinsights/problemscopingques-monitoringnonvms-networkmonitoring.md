
<properties
pageTitle="Network monitoring - NPM, DNS"
description="Network monitoring - NPM, DNS"
articleId="problemscopingques-Network_monitoring_NPM_DNS"
authors="yossiy"
ms.author="yossiy"
selfHelpType="problemScopingQuestions"
supportTopicIds="32626098"
productPesIds="15725"
cloudEnvironments="Public, Fairfax, usnat, ussec"
schemaVersion="1"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# Network monitoring - NPM, DNS
 
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Network monitoring - NPM, DNS",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "solution_added",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Was the solution recently added?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Not sure"
                }
            ],
            "required": true
        },
        {
            "id": "solution_worked",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Has the solution ever worked?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Not sure"
                }
            ],
            "required": true
        },
        {
            "id": "enable_rules_script",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Have you run the 'Enable Rules' script?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Not sure"
                }
            ],
            "required": true
        },
        {
            "id": "unhealthy_nodes",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Are all nodes showing as unhealthy?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Not sure"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 6,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "hints": [
                {
                    "text": "Describe if any resource is showing unhealthy"
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---