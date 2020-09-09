<properties
    pageTitle="Database Extensions"
    description="Database Extensions"
    authors="Xin-Cheng"
    ms.author="chengxin"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32639990"
    productPesIds="17067,17069,17068"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="problemscopingques-pg-extension-issues"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
# Extensions - Issues with extensions
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Database Extensions",
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
            "id": "extension_name",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "What is the name of the extension?",
            "required": true
        },
        {
            "id": "extension_version",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What is the version of the extension?",
            "required": false
        },
        {
            "id": "operation",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "What operation do you want to perform?",
            "dropdownOptions": [
                {
                    "value": "Enable",
                    "text": "Enable"
                },
                {
                    "value": "Disable",
                    "text": "Disable"
                }
            ],
            "required": false
        },
        {
            "id": "error",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the error message that you are getting?",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Problem description",
            "watermarkText": "Provide your repro steps and other information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
