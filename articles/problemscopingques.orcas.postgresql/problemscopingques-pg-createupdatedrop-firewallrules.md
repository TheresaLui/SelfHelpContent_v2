<properties
    pageTitle="Create Update Drop Resources"
    description="Create Update Drop Resources"
    authors="Xin-Cheng"
    ms.author="chengxin"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32639980"
    productPesIds="17067,17069,17068"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="problemscopingques-pg-createupdatedrop-firewallrules"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
# Create Update and Drop Resources - Firewal Rules
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Create Update Drop Resources Firewall",
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
            "id": "same_issue_happened",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "If you have multiple servers, did you experience the same issue on other servers?",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
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
