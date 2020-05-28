
<properties
pageTitle="Create dashboards and views"
description="Create dashboards and views"
articleId="problemscopingques-Create_dashboards_and_views"
authors="yossiy"
ms.author="yossiy"
selfHelpType="problemScopingQuestions"
supportTopicIds="32633016"
productPesIds="15725"
cloudEnvironments="Public, Fairfax, usnat, ussec"
schemaVersion="1"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# Create dashboards and views
---
{
    "resourceRequired": true,
    "title": "Restore deleted workspace",
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
            "id": "is_it_azure_vm",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Where are you seeing the issue?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Azure dashboard",
                    "text": "Azure dashboard"
                },
                {
                    "value": "Solution, or View Designer part",
                    "text": "Solution, or View Designer part"
                },
                {
                    "value": "Power BI",
                    "text": "Power BI"
                },
                {
                    "value": "Grafana",
                    "text": "Grafana"
                },
                {
                    "value": "Other",
                    "text": "Other - please provide information below"
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
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "If you are experiencing failure, what errors are you seeing?",
            "watermarkText": "Enter the error message",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 4,
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