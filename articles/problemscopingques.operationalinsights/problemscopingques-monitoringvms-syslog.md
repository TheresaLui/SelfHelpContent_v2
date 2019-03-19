
<properties
pageTitle="Syslog"
description="Syslog"
articleId="problemscopingques-Syslog"
authors="yossiy"
ms.author="yossiy"
selfHelpType="problemScopingQuestions"
supportTopicIds="32633008"
productPesIds="15725"
cloudEnvironments="Public, Fairfax"
schemaVersion="1"
/>

# Syslog
---
{
    "resourceRequired": true,
    "title": "Syslog",
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
            "id": "syslog_monitoring",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Are you monitoring syslog from a Linux instance or a network device?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Linux instance",
                    "text": "Linux instance"
                },
                {
                    "value": "Network device",
                    "text": "Network device"
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
            "order": 3,
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