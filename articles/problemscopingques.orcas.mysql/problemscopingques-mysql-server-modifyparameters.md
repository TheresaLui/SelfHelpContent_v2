<properties
    pageTitle="Server Parameters"
    description="Server Parameters"
    authors="Hang-Zhang"
    ms.author="haz"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32640070"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax"
    schemaVersion="1"
    articleId="problemscopingques-mysql-server-modify_parameters"
/>
# Server Parameters - Modify server parameters
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Server Parameters Modify",
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
            "id": "server_parameter",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "What server parameter(s) do you want to change?",
            "required": false
        },
        {
            "id": "parameter_value",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What is value you want to change to?",
            "required": false
        },
        {
            "id": "error_message",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the error message you received?",
            "watermarkText": "",
            "required": false,
            "useAsAdditionalDetails": false
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
