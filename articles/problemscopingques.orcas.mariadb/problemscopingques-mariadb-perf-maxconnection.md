<properties
    pageTitle="Database Performance"
    description="Database Performance"
    authors="Hang-Zhang"
    ms.author="haz"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32640153"
    productPesIds="16617"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="problemscopingques-mariadb-perf-max_connection"
	ownershipId="AzureData_AzureDatabaseforMariaDB"
/>
# Performance and Query Execution - Server hit maximum connection limit
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Database Performance Server hit max connectin limit",
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
            "id": "client_driver",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "What is the name and version of the client driver you are using?",
            "required": false
        },
        {
            "id": "host_in_azure",
            "order": 3,
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
            "order": 4,
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
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "What is the normal number of concurrent connections of your workload?",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 6,
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
