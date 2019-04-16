
<properties
pageTitle="Action Group notification not received"
description="Action Group notification not received"
articleId="problemscopingques-Action_Group_notification_not_received"
authors="yossiy"
ms.author="yossiy"
selfHelpType="problemScopingQuestions"
supportTopicIds="32633011"
productPesIds="15725"
cloudEnvironments="Public, Fairfax"
schemaVersion="1"
/>

# Action Group notification not received 
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Action Group notification not received",
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
            "resourceRequired": true,
                "title": "Log Search Alert",
                "fileAttachmentHint": "",
                "formElements": [{
                    "id": "log_alert_id",
                    "order": 1,
                    "controlType": "dropdown",
                    "displayLabel": "Which alert rule has this problem?",
                    "watermarkText": "Choose an alert that has the problem",
                    "dynamicDropdownOptions": {
                        "uri": "/subscriptions/{subscriptionid}/resourceGroups/{resourcegroup}/providers/microsoft.operationalInsights/workspaces/{resource}/rules?api-version=2015-03-20",
                        "jTokenPath": "",
                        "textProperty": "DisplayName",
                        "valueProperty": "id",
                        "textPropertyRegex": "[^/]+$"
                    },
                    "dropdownOptions": [
                        {
                        "value": "Unable to get the list of Alerts",
                        "text": "Unable to get the list of Alerts"
                        }
                    ],
                "required": true
            }
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