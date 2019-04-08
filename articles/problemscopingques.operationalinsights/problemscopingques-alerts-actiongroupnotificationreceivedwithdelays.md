
<properties
pageTitle="Alerts/Action Group notification received with delays"
description="Alerts/Action Group notification received with delays"
articleId="problemscopingques-Alerts_Action_Group_notification_received_with_delays"
authors="yossiy"
ms.author="yossiy"
selfHelpType="problemScopingQuestions"
supportTopicIds="32633012"
productPesIds="15725"
cloudEnvironments="Public, Fairfax"
schemaVersion="1"
/>

# Alerts/Action Group notification received with delays 
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Alerts/Action Group notification received with delays",
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
            "id": "action_group_type",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Which notification type has the problem?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Email",
                    "text": "Email"
                },
                {
                    "value": "SMS",
                    "text": "SMS"
                },
                {
                    "value": "Webhook",
                    "text": "Webhook"
                },
                {
                    "value": "Logic app",
                    "text": "Logic app"
                },
                {
                    "value": "Runbook",
                    "text": "Runbook"
                },
                {
                    "value": "ITSM",
                    "text": "ITSM"
                },
                {
                    "value": "Voice/Phone call",
                    "text": "Voice/Phone call"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Not sure"
                }
            ],
            "required": true
        },
        {
            "id": "alert_rule",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Which alert rule has this problem?",
            "watermarkText": "Enter alert rule name",
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
    ]
}
---