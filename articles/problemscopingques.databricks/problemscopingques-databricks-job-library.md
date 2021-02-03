<properties
	articleId="dc5a7fad-9998-4d90-a61d-9ca57a9ef5a4"
	pageTitle="Scoping Questions for Databricks Job Issue related to library"
	description="Scoping Questions for Databricks Job Issue related to library"
	authors="lisaliu"
	ms.author="lisaliu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32742957"
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_AzureDatabricks"
/>
# Databricks Cluster Job Issue
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Azure Databricks Job Issue",
    "fileAttachmentHint": "Please attach log from the API, Airflow, or ADF",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "What time did the problem begin?",
            "required": true
        },
        {
            "id": "problem_end_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate time when the problem stopped occurring. If the issue is ongoing, leave this field blank",
            "required": false
        },
        {
            "id": "errormessage",
            "order": 30,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the error message you received?",
            "watermarkText": "Please copy and paste the complete error text including the stack trace if available",
            "required": false
        },
        {
            "id": "library",
            "order": 40,
            "controlType": "multilinetextbox",
            "displayLabel": "What libraries are being installed?",
            "watermarkText": "",
            "required": false
        },
        {
            "id": "librarysource",
            "order": 50,
            "controlType": "dropdown",
            "displayLabel": "What repository or location are the libraries stored?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Maven",
                    "text": "Maven"
                },
                {
                    "value": "PyPI",
                    "text": "PyPI"
                },
                {
                    "value": "CRAN",
                    "text": "CRAN"
                },
                {
                    "value": "DBFS",
                    "text": "DBFS"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "is_new_problem",
            "order": 100,
            "controlType": "dropdown",
            "displayLabel": "Is this a new problem, or it has happened before?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "New_problem",
                    "text": "New problem, worked before"
                },
                {
                    "value": "Never_worked",
                    "text": "Never worked"
                },
                {
                    "value": "Happened_before",
                    "text": "Not new, happened before"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "previous_solution",
            "visibility": "is_new_problem == Happened_before",
            "order": 110,
            "controlType": "multilinetextbox",
            "displayLabel": "Previous solution if applicable",
            "watermarkText": "If the previous occurance was resolved, please share how it was resolved",
            "required": false
        },
        {
            "id": "change_made",
            "visibility": "is_new_problem == New_problem",
            "order": 120,
            "controlType": "multilinetextbox",
            "displayLabel": "Any changes made?",
            "watermarkText": "Any changes since last time it worked",
            "required": false
        },
        {
            "id": "cluster_url",
            "order": 170,
            "controlType": "textbox",
            "displayLabel": "Cluster URL",
            "infoBalloonText": "Follow this <a href='https://docs.microsoft.com/azure/databricks/workspace/workspace-details#cluster-url-and-id'>article</a> to get Cluster URL",
            "required": true
        },
        {
            "id": "job_rul",
            "order": 300,
            "controlType": "textbox",
            "displayLabel": "Job URL for the job with issue",
            "infoBalloonText": "Follow <a href='https://docs.microsoft.com/azure/databricks/workspace/workspace-details#job-url-and-id'>this article</a> to get Job URL",
            "required": false
        },
        {
            "id": "job_rul_goodrun",
            "order": 400,
            "controlType": "textbox",
            "displayLabel": "Job URL from last known good run if available",
            "infoBalloonText": "Follow <a href='https://docs.microsoft.com/azure/databricks/workspace/workspace-details#job-url-and-id'>this article</a> to get Job URL",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 600,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional details about the issue",
            "watermarkText": "Please provide the detail symptom including the full error text, whether the issue is intermittent or persistent, and any other relevant information",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
