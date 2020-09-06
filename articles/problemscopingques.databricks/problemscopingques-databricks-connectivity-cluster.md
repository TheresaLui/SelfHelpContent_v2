<properties
	articleId="25bdb17b-54b0-4385-bd03-c04e2fdf6480"
	pageTitle="Scoping Questions for Databricks Connectivity to Cluster Issue"
	description="Scoping Questions for Databricks Connectivity to Cluster Issue"
	authors="lisaliu"
	ms.author="lisaliu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32677672"
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_AzureDatabricks"
/>
# Databricks Cluster Connectivity Issue
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Azure Databricks Connectivity Issue",
    "fileAttachmentHint": "",
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
            "displayLabel": "What error message you received?",
            "watermarkText": "Please copy paste the full error text including the stack trace if available",
            "required": false
        },
        {
            "id": "is_new_problem",
            "order": 50,
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
            "required": true
        },
        {
            "id": "change_made",
            "visibility": "is_new_problem == New_problem",
            "order": 120,
            "controlType": "multilinetextbox",
            "displayLabel": "Any changes made?",
            "watermarkText": "Any changes since last time it worked",
            "required": true
        },
        {
            "id": "cluster_url",
            "order": 150,
            "controlType": "textbox",
            "displayLabel": "Cluster URL if available",
            "infoBalloonText": "Follow this <a href='https://docs.microsoft.com/azure/databricks/workspace/workspace-details#cluster-url-and-id'>article</a> to get Cluster URL",
            "required": true
        },
        {
            "id": "workspace_id",
            "order": 170,
            "controlType": "textbox",
            "displayLabel": "Workspace ID if cluster URL is not available",
            "infoBalloonText": "Follow this <a href='https://docs.microsoft.com/azure/databricks/workspace/workspace-details#per-workspace-url'>article</a> to get Workspace ID",
            "required": false
        },
        {
            "id": "connect_from",
            "order": 250,
            "controlType": "dropdown",
            "displayLabel": "How are you connecting to the workspace",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "job",
                    "text": "Job"
                },
                {
                    "value": "notebook",
                    "text": "Notebook"
                },
                {
                    "value": "restAPI",
                    "text": "REST API"
                },
                {
                    "value": "dbconnect",
                    "text": "Databricks Connect"
                },
                {
                    "value": "odbc",
                    "text": "ODBC client application"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "connectfromjob",
            "visibility": "connect_from == job",
            "order": 300,
            "controlType": "textbox",
            "displayLabel": "Job URL for the job with the connectivity issue",
            "infoBalloonText": "Follow <a href='https://docs.microsoft.com/azure/databricks/workspace/workspace-details#job-url-and-id'>this article</a> to get Job URL",
            "required": true
        },
        {
            "id": "connectfromnotebook",
            "visibility": "connect_from == notebook",
            "order": 350,
            "controlType": "textbox",
            "displayLabel": "Notebook URL for the Notebook with the connectivity issue",
            "infoBalloonText": "Follow <a href='https://docs.microsoft.com/azure/databricks/workspace/workspace-details#--notebook-url-and-id'>this article</a> to get Notebook URL",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 600,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional details about the issue",
            "watermarkText": "Please provide any additional information related to this issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
