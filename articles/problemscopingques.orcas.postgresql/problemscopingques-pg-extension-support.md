<properties
    pageTitle="Database Extensions"
    description="Database Extensions"
    authors="Xin-Cheng"
    ms.author="chengxin"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32640016"
    productPesIds="16222"
    cloudEnvironments="public"
    schemaVersion="1"
    articleId="problemscopingques-pg-extension-support"
/>
# Extensions - Request support for new extension
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
            "required": true
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
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know or unsure"
                }
            ],
            "required": true
        },
        {
            "id": "problem_description",
            "order": 5,
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
