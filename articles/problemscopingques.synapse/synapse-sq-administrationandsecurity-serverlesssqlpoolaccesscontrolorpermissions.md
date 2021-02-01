<properties
    schemaVersion = "1"
    selfHelpType = "problemScopingQuestions"
    cloudEnvironments = "public, fairfax, blackforest, mooncake, usnat, ussec"
    ownershipId = "AzureData_SynapseAnalytics"
    productPesIds = "15818"
    supportTopicIds = "32783903"
    pageTitle = "Administration and Security/Serverless SQL pool - Access control or permissions"
    description = "Administration and Security/Serverless SQL pool - Access control or permissions"
    articleId = "synapse-sq-administrationandsecurity-serverlesssqlpoolaccesscontrolorpermissions.md"
    ms.author = "fipopovi, saltug"
/>

# Administration and Security/Serverless SQL pool - Access control or permissions

---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": true,
    "fileAttachmentHint": "",
    "title": "Serverless SQL pool - Access control or permissions",
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
            "id": "sqlod_2",
            "order": 2,
            "required": false,
            "controlType": "multilinetextbox",
            "displayLabel": "If an error was displayed, what was the error message (including distributed statement id, if any)?",
            "watermarkText": "",
            "infoBalloonText": ""
        },
        {
            "id": "sqlod_3",
            "order": 3,
            "required": false,
            "controlType": "dropdown",
            "displayLabel": "Do you use AAD or SQL login?",
            "watermarkText": "",
            "infoBalloonText": "",
            "dropdownOptions": [
                {
                    "value": "Azure Active Directory",
                    "text": "Azure Active Directory"
                },
                {
                    "value": "SQL",
                    "text": "SQL"
                }
            ]
        },
        {
            "id": "sqlod_4",
            "order": 4,
            "required": false,
            "controlType": "dropdown",
            "displayLabel": "What storage account type do you want to query? (Blob Storage, ADLS Gen1, ADLS Gen2)",
            "watermarkText": "",
            "infoBalloonText": "",
            "dropdownOptions": [
                {
                    "value": "Blob Storage",
                    "text": "Blob Storage"
                },
                {
                    "value": "ADLS Gen1",
                    "text": "ADLS Gen1"
                },
                {
                    "value": "ADLS Gen2",
                    "text": "ADLS Gen2"
                },
                {
                    "value": "Other",
                    "text": "Other"
                }
            ]
        },
        {
            "id": "sqlod_5",
            "order": 5,
            "required": false,
            "controlType": "dropdown",
            "displayLabel": "What type of credential do you use? (UserIdentity, ManagedIdentity, SAS)",
            "watermarkText": "",
            "infoBalloonText": "",
            "dropdownOptions": [
                {
                    "value": "UserIdentity",
                    "text": "UserIdentity"
                },
                {
                    "value": "ManagedIdentity",
                    "text": "ManagedIdentity"
                },
                {
                    "value": "SAS",
                    "text": "SAS"
                },
                {
                    "value": "Other",
                    "text": "Other"
                }
            ]
        },
        {
            "id": "problem_description",
            "order": 6,
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


