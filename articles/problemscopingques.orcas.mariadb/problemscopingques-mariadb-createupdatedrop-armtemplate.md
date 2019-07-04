<properties
    pageTitle="Create Update Drop Resources"
    description="Create Update Drop Resources"
    authors="Hang-Zhang"
    ms.author="haz"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32640111"
    productPesIds="16617"
    cloudEnvironments="public"
    schemaVersion="1"
    articleId="problemscopingques-mariadb-createupdatedrop-arm_template"
/>
# Create Update and Drop Resources - ARM template issues
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Create Update Drop Resources ARM Template",
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
            "id": "arm_template",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Can you provide the sample ARM template you are using? Please remove the sensitive information (such as password) from the sample.",
            "required": false
        },
        {
            "id": "operation_request_from",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Did you submit the operation request from the Azure portal or Azure CLI?",
            "dropdownOptions": [
                {
                    "value": "Azure portal",
                    "text": "Azure portal"
                },
                {
                    "value": "Azure CLI",
                    "text": "Azure CLI"
                },
                {
                    "value": "I don't have the answer",
                    "text": "I don't have the answer"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 4,
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
