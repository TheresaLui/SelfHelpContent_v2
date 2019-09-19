<properties
    pageTitle="Scoping questions for Query performance and timeouts"
    description="Query performance and timeouts"
    service="microsoft.sql"
    authors="pxding,vitomaz-msft,MladjoA"
    ms.author="vitomaz"
    articleId="problemscopingques-sqlmi-perfqueryexecution-queryperformanceandtimeouts"
    selfHelpType="ProblemScopingQuestions"
    supportTopicIds="32637296"
    productPesIds="16259"
    cloudEnvironments="public,blackForest,fairfax,mooncake"
    schemaVersion="1"
/>

# Query performance and timeouts
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Query performance and timeouts",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },{
            "id": "problem_end_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem stop? (If ongoing, leave this field blank)?",
            "required": false
        },{
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Specific Query Store query_id, plan hash, query hash or query text.",
            "watermarkText": "Provide additional information about your query performance and timeouts.",
            "required": true
        }
    ]
}
---
