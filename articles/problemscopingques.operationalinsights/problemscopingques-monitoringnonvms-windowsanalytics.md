
<properties
pageTitle="Windows Analytics - Upgrade Readiness, Device Health, Update Compliance"
description="Windows Analytics - Upgrade Readiness, Device Health, Update Compliance"
articleId="problemscopingques-Windows_Analytics_Upgrade_Readiness_Device_Health_Update_Compliance"
authors="yossiy"
ms.author="yossiy"
selfHelpType="problemScopingQuestions"
supportTopicIds="32612530"
productPesIds="15725"
cloudEnvironments="Public, Fairfax, usnat, ussec"
schemaVersion="1"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# Windows Analytics - Upgrade Readiness, Device Health, Update Compliance
 
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Windows Analytics - Upgrade Readiness, Device Health, Update Compliance",
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
            "id": "single_machine",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Is there a problem with a single machine or all machines?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Single machine",
                    "text": "Single machine"
                },
                {
                    "value": "All machines",
                    "text": "All machines"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Not sure"
                }
            ],
            "required": true
        },
        {
            "id": "error_message",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "Name of a sample machine that is not working",
            "watermarkText": "Enter machine name",
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
            "hints": []
        }
    ],
    "$schema": "SelfHelpContent"
}
---