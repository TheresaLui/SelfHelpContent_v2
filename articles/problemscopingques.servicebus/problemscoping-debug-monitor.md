<properties
pageTitle="Issues with Monitoring"
description="Issues with Monitoring"
service="microsoft.servicebus"
resource="monitorIssueTypes"
authors="mksuni"
ms.author="mksuni"
displayOrder=""
selfHelpType="problemScopingQuestions"
supportTopicIds="32633402"
resourceTags=""
productPesIds="13186"
cloudEnvironments="public, Fairfax, usnat, ussec"
articleId="sb-debug-monitor"
schemaVersion="1"
	ownershipId="AzureMessaging_Common"
/>
# Monitor and Debug 
---
{
    "subscriptionRequired": true,
    "title": "Issues with Monitoring",
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
            "id": "problem_metrics",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Please include the type of metrics you are trying to setup?",
            "required": false
        },
        {
            "id": "problem_alert",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Please include the type of alerts you are trying to setup?",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Issue description."
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---