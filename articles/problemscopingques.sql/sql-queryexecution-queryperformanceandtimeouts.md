<properties
	pageTitle="Scoping questions for Query performance and timeouts"
	description="Query performance and timeouts"
	service="microsoft.sql"
	authors="pxding"
        ms.author="pedin"
        articleId="C00BD8E2-3CA0-451D-A2E5-8BE0987A0150"
        selfHelpType="ProblemScopingQuestions"
        supportTopicIds="32630450"
        productPesIds="13491"
	cloudEnvironments="public,blackForest,fairfax,mooncake"
        schemaVersion="1"
	ownershipId="AzureData_AzureSQLDB"
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
            "displayLabel": "What is the start time of the issue?",
            "required": true
        },{
            "id": "problem_end_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "What is the end time of the issue?",
            "required": true
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

