<properties
    pageTitle="Create Update Drop Resources"
    description="Create Update Drop Resources"
    authors="Hang-Zhang"
    ms.author="haz"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32747636"
    productPesIds="17344"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="scoping-mysql-flexsvr-createupdatedrop-server"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>
# Create Update and Drop Resources - Server
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Create Update Drop Resources Server",
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
            "id": "error_message",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the error message you received?",
            "watermarkText": "",
            "required": false,
            "useAsAdditionalDetails": false
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
                    "value": "dont_know_answer",
                    "text": "Don't know or unsure"
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
