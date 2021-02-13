<properties
    pageTitle="Portal, Client Tools and APIs"
    description="Portal, Client Tools and APIs"
    authors="seanliang"
    ms.author="zhlian"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32639972, 32780895, 32780905"
    productPesIds="17067,17068,17069"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="problemscopingques-pg-portalclient-driver"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
# Portal, Client Tools and APIs - Client drivers and API's
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Tools and APIs Client drivers and API's",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Azure Database for PostgreSQL Portal, Client Tools and APIs Troubleshooter",
        "description": "Our Azure Database for PostgreSQL Portal, Client Tools and APIs Troubleshooter can help you troubleshoot and solve your problem.",
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
            "id": "driver_name",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What is the name of the driver you are using?",
            "required": true
        },
        {
            "id": "driver_version",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "What is the version of the driver you are using?",
            "required": false
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
