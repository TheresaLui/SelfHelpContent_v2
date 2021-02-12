
<properties
pageTitle="Alert fires when it should not"
description="Alert fires when it should not"
articleId="problemscopingques-Alert_fires_when_it_should_not"
authors="yossiy"
ms.author="yossiy"
selfHelpType="problemScopingQuestions"
supportTopicIds="32612427"
productPesIds="15725"
cloudEnvironments="Public, Fairfax, usnat, ussec"
schemaVersion="1"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# Alert fires when it should NOT
 
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Alert fires when it should NOT",
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