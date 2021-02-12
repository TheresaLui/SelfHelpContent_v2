<properties
    pageTitle="Security"
    description="Security"
    authors="Xin-Cheng"
    ms.author="chengxin"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32639989, 32780939, 32780947"
    productPesIds="16222,17067,17069"
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
    "diagnosticCard": {
        "title": "Azure Database for PostgreSQL Security Troubleshooter",
        "description": "Our Azure Database for Security Troubleshooter can help you troubleshoot and solve your problem.",
        "insightNotAvailableText": "Our troubleshooter did not detect any issues with your resource. Following the steps in Recommended Solution section below to troubleshoot your problem."
    },
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "infoBalloonText": "Enter the approximate time you started to see the error.",
            "required": true,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "problem_end_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem stop? (If ongoing, leave this field blank)",
            "infoBalloonText": "Enter when the error stopped, or leave blank if the issue is ongoing.",
            "required": false,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "permission_required",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What permissions are you looking for?",
            "required": false
        },
        {
            "id": "query_executed",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Can you share the query you cannot execute due to lack of super user permission?",
            "watermarkText": "",
            "required": false,
            "useAsAdditionalDetails": false
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Problem description",
            "watermarkText": "Please provide the repro steps and other information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
