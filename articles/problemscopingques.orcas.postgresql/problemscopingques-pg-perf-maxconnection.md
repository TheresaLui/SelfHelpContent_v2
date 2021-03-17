<properties
    pageTitle="Database Performance"
    description="Database Performance"
    authors="Xin-Cheng"
    ms.author="chengxin"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32640019, 32781009, 32781010"
    productPesIds="17067,17068,17069"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="problemscopingques-pg-perf-maxconnection"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>
# Performance and Query Execution - Server hit maximum connection limit
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Database Performance Server hit max connectin limit",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Azure Database for PostgreSQL Perf Troubleshooter",
        "description": "Our Azure Database for PostgreSQL Perf Troubleshooter can help you troubleshoot and solve your problem.",
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
            "id": "client_driver",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What is the name and version of the client driver you are using?",
            "required": false
        },
        {
            "id": "host_in_azure",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Is your client hosted within Azure?",
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
            "id": "connection_pool",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Are you using a connection pool?",
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
            "id": "number_concurrency",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "What is the normal number of concurrent connections of your workload?",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 7,
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
