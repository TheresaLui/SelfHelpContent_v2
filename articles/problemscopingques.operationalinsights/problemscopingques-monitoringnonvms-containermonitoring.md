
<properties
pageTitle="Container monitoring"
description="Container monitoring"
articleId="problemscopingques-Container_monitoring"
authors="yossiy"
ms.author="yossiy"
selfHelpType="problemScopingQuestions"
supportTopicIds="32745413"
productPesIds="15725"
cloudEnvironments="Public, Fairfax, usnat, ussec"
schemaVersion="1"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# Container monitoring
---
{
    "resourceRequired": true,
    "title": "Container monitoring",
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
            "id": "what_container_monitoring_tools",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What container monitoring tools are you using?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Azure Monitor for Container, aka Container Insights",
                    "text": "Azure Monitor for Container, aka Container Insights"
                },
                {
                    "value": "Container Monitoring Solution",
                    "text": "Container Monitoring Solution"
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