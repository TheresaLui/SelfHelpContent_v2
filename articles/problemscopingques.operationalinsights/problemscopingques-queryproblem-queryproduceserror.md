
<properties
pageTitle="Query produces error, times out or too slow"
description="Query produces error, times out or too slow"
articleId="problemscopingques-Query_produces_error_times_out_or_too_slow"
authors="yossiy"
ms.author="yossiy"
selfHelpType="problemScopingQuestions"
supportTopicIds="32612514"
productPesIds="15725"
cloudEnvironments="Public, Fairfax, usnat, ussec"
schemaVersion="1"
	ownershipId="AzureMonitoring_LogAnalytics"
/>

# Query produces error, times out or too slow 
---
{
    "resourceRequired": true,
    "title": "Query produces error, times out or too slow",
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
            "id": "request_id",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "What is the request id for the query (can be copied from Logs portal, on the right side above the results pane)?",
            "watermarkText": "Enter request id",
            "required": false
        },
        {
            "id": "attachment",
            "order": 3,
            "controlType": "infoblock",
            "content": "Please attach or paste in the query and expected results"
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
    ],
    "$schema": "SelfHelpContent"
}
---