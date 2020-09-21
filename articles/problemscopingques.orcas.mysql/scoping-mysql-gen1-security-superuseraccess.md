<properties
    pageTitle="Security"
    description="Security"
    authors="Hang-Zhang"
    ms.author="haz"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32747566"
    productPesIds="17343"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="scoping-mysql-gen1-security-superuser_access"
	ownershipId="AzureData_AzureDatabaseforMySQL"
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
