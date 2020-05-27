
<properties
pageTitle="SCOM integration or OMS Gateway"
description="SCOM integration or OMS Gateway"
articleId="problemscopingques-SCOM_integration_or_OMS_Gateway"
authors="yossiy"
ms.author="yossiy"
selfHelpType="problemScopingQuestions"
supportTopicIds="32633006"
productPesIds="15725"
cloudEnvironments="Public, Fairfax, usnat, ussec"
schemaVersion="1"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# SCOM integration or OMS Gateway
---
{
    "resourceRequired": true,
    "title": "SCOM integration or OMS Gateway",
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
            "id": "integration_worked",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Has the integration/gateway ever worked?",
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
            "id": "scom_version",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What version of SCOM are you using?",
            "watermarkText": "Enter SCOM version",
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