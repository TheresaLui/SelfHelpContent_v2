<properties
pageTitle="Monitoring and Metrics Issues"
description="Monitoring and Metrics Issues"
service="microsoft.relay"
resource="monitoringissues"
authors="mksuni"
ms.author="mksuni"
displayOrder=""
selfHelpType="problemScopingQuestions"
supportTopicIds="32684544"
resourceTags=""
productPesIds="16123"
cloudEnvironments="public, Fairfax, usnat, ussec"
articleId="relay-monitor"
schemaVersion="1"
	ownershipId="AzureMessaging_Common"
/>
# Monitoring and Metrics Issues
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Monitoring and Metrics Issues",
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
            "id": "problem_alerts",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "What alerts are your trying to create",
            "required": false
        },
       {
            "id": "problem_metrics",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": " Are you trying to create metrics or alerts on Hybrid Connections",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide exact error message if appicable . Also provide any additional details if any  ",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---