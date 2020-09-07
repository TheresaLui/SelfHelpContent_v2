<properties
    pageTitle="Security"
    description="Security"
    authors="Xin-Cheng"
    ms.author="chengxin"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32639989"
    productPesIds="17067,17069,17068"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="problemscopingques-pg-security-superuseraccess"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
# Security - I need superuser access
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Security Superuser Access",
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
            "id": "permission_required",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "What permissions are you looking for?",
            "required": false
        },
        {
            "id": "query_executed",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Can you share the query you cannot execute due to lack of super user permission?",
            "watermarkText": "",
            "required": false,
            "useAsAdditionalDetails": false
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
