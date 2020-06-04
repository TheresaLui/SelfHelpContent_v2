
<properties
pageTitle="Alert doesn’t fire when it should"
description="Alert doesn’t fire when it should"
articleId="problemscopingques-Alert_doesnt_fire_when_it_SHOULD"
authors="yossiy"
ms.author="yossiy"
selfHelpType="problemScopingQuestions"
supportTopicIds="32612428"
productPesIds="15725"
cloudEnvironments="Public, Fairfax, usnat, ussec"
schemaVersion="1"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# Alert doesn’t fire when it SHOULD
 
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Alert doesn’t fire when it SHOULD",
    "fileAttachmentHint": "Provide screenshot of alert rule configuration with query and query results in Logs",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "alert_rule",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Which alert rule has this problem?",
            "watermarkText": "Enter alert rule name",
            "required": false
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
    ],
    "$schema": "SelfHelpContent"
}
---