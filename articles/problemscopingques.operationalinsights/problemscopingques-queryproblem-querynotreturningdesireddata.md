
<properties
pageTitle="Query not returning desired data "
description="Query not returning desired data "
articleId="problemscopingques-Query_not_returning_desired_data "
authors="yossiy"
ms.author="yossiy"
selfHelpType="problemScopingQuestions"
supportTopicIds="32612517"
productPesIds="15725"
cloudEnvironments="Public, Fairfax"
schemaVersion="1"
	ownershipId="ASEP_ContentService_Placeholder"
/>

# Query not returning desired data 
---
{
    "resourceRequired": true,
    "title": "Query not returning desired data ",
    "fileAttachmentHint": "Please attach or paste in the query and expected results",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "query_call",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What method are you using for the query?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Logs in Log Analytics workspace",
                    "text": "Logs in Log Analytics workspace"
                },
                {
                    "value": "Logs in Azure Monitor",
                    "text": "Logs in Azure Monitor"
                },
                {
                    "value": "Grafana",
                    "text": "Grafana"
                },
                {
                    "value": "API",
                    "text": "API"
                },
                {
                    "value": "Other",
                    "text": "Other"
                },
                {
                    "value": "dont_know_answer",
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
    ],
    "$schema": "SelfHelpContent"
}
---