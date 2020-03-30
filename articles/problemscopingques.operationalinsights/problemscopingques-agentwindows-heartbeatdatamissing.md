
<properties
pageTitle="Agent not reporting data or Heartbeat data missing"
description="Agent not reporting data or Heartbeat data missing"
articleId="problemscopingques-Windows_Agent not reporting data or Heartbeat data missing"
authors="yossiy"
ms.author="yossiy"
selfHelpType="problemScopingQuestions"
supportTopicIds="32612463"
productPesIds="15725"
cloudEnvironments="Public, Fairfax"
schemaVersion="1"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# Agent not reporting data or Heartbeat data missing
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
            "id": "single_multiple_machines",
            "order": 2,
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
            "id": "is_it_azure_vm",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Is this an Azure VM?",
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
            "id": "flush_agent",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Have you tried to flush the agent cache?",
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
            "id": "error_message",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "What error are you seeing?",
            "watermarkText": "Enter the error message",
            "required": false
        },
        {
            "id": "affected_machine",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "What's the name of an affected machine? If there are multiple, please include a few names",
            "watermarkText": "Enter the name of the machine(s)",
            "required": false
        },
        {
            "id": "agen_version",
            "order": 7,
            "controlType": "textbox",
            "displayLabel": "What version of Windows are you running?",
            "watermarkText": "Enter the Windows version",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 8,
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