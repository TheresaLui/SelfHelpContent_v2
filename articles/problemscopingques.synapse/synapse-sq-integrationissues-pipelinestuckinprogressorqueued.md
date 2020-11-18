<properties
    schemaVersion = "1"
    selfHelpType = "problemScopingQuestions"
    cloudEnvironments = "public, fairfax, blackforest, mooncake, usnat, ussec"
    ownershipId = "AzureData_SynapseAnalytics"
    productPesIds = "15818"
    supportTopicIds = "32783899"
    pageTitle = "Integration Issues/Pipeline stuck in progress or queued"
    description = "Integration Issues/Pipeline stuck in progress or queued"
    articleId = "synapse-sq-integrationissues-pipelinestuckinprogressorqueued.md"
    ms.author = "saltug"
/>

# Integration Issues/Pipeline stuck in progress or queued

---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": true,
    "fileAttachmentHint": "",
    "title": "Pipeline Stuck in Progress or Queued",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "required": true,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start",
            "infoBalloonText": ""
        },
        {
            "id": "sq_2",
            "order": 2,
            "required": false,
            "controlType": "textbox",
            "displayLabel": "If an error was displayed, what was the error message?",
            "watermarkText": "",
            "infoBalloonText": ""
        },
        {
            "id": "source_name",
            "order": 3,
            "required": false,
            "controlType": "TextBox",
            "displayLabel": "What's the source of the slow activity?",
            "watermarkText": "",
            "infoBalloonText": ""
        },
        {
            "id": "sink_name",
            "order": 4,
            "required": false,
            "controlType": "TextBox",
            "displayLabel": "What's the sink of the slow activity?",
            "watermarkText": "",
            "infoBalloonText": ""
        },
        {
            "id": "ir_type",
            "order": 5,
            "required": true,
            "controlType": "DropDown",
            "displayLabel": "Which type of integration runtime are you using?",
            "watermarkText": "Choose an IR type",
            "infoBalloonText": "",
            "content": null,
            "dropdownOptions": [
                {
                    "text": "Azure IR",
                    "value": "Azure IR"
                },
                {
                    "text": "Self-hosted IR",
                    "value": "Self-hosted IR"
                },
                {
                    "text": "Not applicable",
                    "value": "dont_know_answer"
                }
            ]
        },
        {
            "id": "problem_run_id",
            "order": 6,
            "required": true,
            "controlType": "TextBox",
            "displayLabel": "Pipeline RunIDs with issue (separate with commas)",
            "watermarkText": "",
            "infoBalloonText": ""
        },
        {
            "id": "problem_description",
            "order": 3,
            "required": true,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "infoBalloonText": "",
            "useAsAdditionalDetails": true
        }
    ]
}
---


