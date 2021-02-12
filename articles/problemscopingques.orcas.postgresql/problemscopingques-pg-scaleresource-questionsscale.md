<properties
    pageTitle="Scaling a resource"
    description="Scaling a resource"
    authors="Xin-Cheng"
    ms.author="chengxin"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32640014, 32780927, 32780933"
    productPesIds="17067,17068,17069"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="problemscopingques-pg-scaleresource-questionsscale"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
# Scaling a resource - Questions about scaling a resource
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Scaling Resource Questions",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Azure Database for PostgreSQL Scaling A Resource Troubleshooter",
        "description": "Our Azure Database for Scaling A Resource Troubleshooter can help you troubleshoot and solve your problem.",
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
            "id": "price_tier",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What is the Pricing Tier of your server?",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 4,
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