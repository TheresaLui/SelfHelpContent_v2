<properties
    pageTitle="Query Failures Problem Scoping Questions"
    description="Scoping questions to capture start time for query failures"
    authors="radennis"
    ms.author="prvavill"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32613464,32613482,32613506"
    productPesIds="16602"
    cloudEnvironments="Public, fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="9445526A-2D4B-41D8-9DE4-B19B4D64F397"
    ownershipId="AzureDataExplorer_Kusto"
/>
# Azure Data Explorer Query Failures
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Azure Data Explorer query failures troubleshooter",
    "fileAttachmentHint": "",
     "diagnosticCard": {
        "title": "Query failures diagnostics",
        "description": "These diagnostics will check for query failures.",
        "insightNotAvailableText": "Our troubleshooter did not detect any issues with your resource or Diagnostic generation is taking longer than expected to complete"
    },
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "RootActivityId",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Do you have RootactivityId of the affected query?",
            "watermarkText": "",
            "required": false,
            "diagnosticInputRequiredClients": "Portal, ASC"
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional details",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ]
}
---