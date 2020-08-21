
<properties
pageTitle="Update Management"
description="Update Management"
articleId="problemscopingques-Update_Management"
authors="yossiy"
ms.author="yossiy"
selfHelpType="problemScopingQuestions"
supportTopicIds="32745415"
productPesIds="15725"
cloudEnvironments="Public, Fairfax, usnat, ussec"
schemaVersion="1"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# Update Management
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Update Management",
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
            "id": "single_multiple_machines",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Are you having a problem with the linked automation acccount?",
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
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "single_multiple_machines",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Is the issue on a single machine or multiple machines?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Single machine",
                    "text": "Single machine"
                },
                {
                    "value": "Multiple machines",
                    "text": "Multiple machines"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Not sure"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "affected_machine",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "What's the name of an affected machine? If there are multiple, please include a few names",
            "watermarkText": "Enter the name of the machine(s)",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "hints": [
                {
                    "text": "Include the exact text of any error messages that occur"
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---