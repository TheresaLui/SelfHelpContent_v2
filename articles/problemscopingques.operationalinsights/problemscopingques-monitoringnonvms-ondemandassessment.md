
<properties
pageTitle="Assessment – On-demand and Health Check (Active Directory, SQL)"
description="Assessment – On-demand and Health Check (Active Directory, SQL)"
articleId="problemscopingques-Assessment"
authors="yossiy"
ms.author="yossiy"
selfHelpType="problemScopingQuestions"
supportTopicIds="32612423"
productPesIds="15725"
cloudEnvironments="Public, Fairfax, usnat, ussec"
schemaVersion="1"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# Assessment – On-demand and Health Check (Active Directory, SQL)
---
{
    "resourceRequired": true,
    "title": "Assessment – On-demand and Health Check (Active Directory, SQL)",
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
            "id": "did_it_work",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Has the assessment ever worked?",
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
            "id": "recently_added",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Was the assessment recently added?",
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
            "id": "assessment_name",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Which assessment do you need help with?",
            "watermarkText": "Enter assessment name",
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
            "hints": []
        }
    ],
    "$schema": "SelfHelpContent"
}
---