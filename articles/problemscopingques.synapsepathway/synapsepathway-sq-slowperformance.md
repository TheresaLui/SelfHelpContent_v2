<properties
    schemaVersion = "1"
    selfHelpType = "problemScopingQuestions"
    cloudEnvironments = "public, fairfax, blackforest, mooncake, usnat, ussec"
    ownershipId = "AzureData_SynapseAnalytics"
    productPesIds = "17487"
    supportTopicIds = "32788657"
    pageTitle = "Slow performance"
    description = "Slow performance"
    articleId = "synapsepathway-sq-slowperformance.md"
    ms.author = "goventur"
/>

# Slow performance

---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": false,
    "resourceRequired": false,
    "fileAttachmentHint": "",
    "title": "Slow performance",
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
            "id": "source_db_system",
            "order": 2,
            "required": false,
            "controlType": "textbox",
            "displayLabel": "What is the source database system?",
            "watermarkText": "Ex: IBM Netezza, Microsoft SQL Server, Snowflake",
            "infoBalloonText": ""
        },
        {
            "id": "source_db_version",
            "order": 3,
            "required": false,
            "controlType": "textbox",
            "displayLabel": "What is the version of the source database system?",
            "watermarkText": "Ex: 7.2, 2019, 4.32",
            "infoBalloonText": ""
        },
        {
            "id": "script_total_size",
            "order": 4,
            "required": false,
            "controlType": "textbox",
            "displayLabel": "What is the total size of the source scripts?",
            "watermarkText": "",
            "infoBalloonText": ""
        },
        {
            "id": "script_total_files",
            "order": 5,
            "required": false,
            "controlType": "textbox",
            "displayLabel": "What is the total number of source scripts?",
            "watermarkText": "",
            "infoBalloonText": ""
        },
        {
            "id": "is_reproducible",
            "order": 6,
            "required": false,
            "controlType": "radioButtonGroup",
            "displayLabel": "Is the problem reproducible?",
            "radioButtonOptions": [{
                    "value": "Yes",
                    "text": "Yes"
                }, {
                    "value": "No",
                    "text": "No"
                }
            ]
        },
        {
            "id": "problem_description",
            "order": 7,
            "required": true,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue (include error message and steps to reproduce, if applicable)",
            "infoBalloonText": "",
            "useAsAdditionalDetails": true
        }
    ]
}
---



