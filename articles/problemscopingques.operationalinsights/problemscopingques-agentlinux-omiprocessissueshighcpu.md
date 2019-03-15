
<properties
pageTitle="OMI process issues: Running high CPU"
description="OMI process issues: Running high CPU"
articleId="problemscopingques-Linux_OMI process issues: Running high CPU"
authors="yossiy"
ms.author="yossiy"
selfHelpType="problemScopingQuestions"
supportTopicIds="32612495"
productPesIds="15725"
cloudEnvironments="Public, Fairfax"
schemaVersion="1"
/>

# OMI process issues: Running high CPU
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
                    "value": "Not sure",
                    "text": "Not sure"
                }
            ],
            "required": true
        },
        {
            "id": "issue_recurrence",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Is this issue constant or does it cycle?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Constant",
                    "text": "Constant"
                },
                {
                    "value": "Cycle",
                    "text": "Cycle"
                },
                {
                    "value": "Not sure",
                    "text": "Not sure"
                }
            ],
            "required": true
        },
        {
            "id": "agent_restart",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Does restarting the agent resolve the issue?",
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
                    "value": "Not sure",
                    "text": "Not sure"
                }
            ],
            "required": true
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
    ]
}
---