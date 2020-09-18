<properties
	articleId="596cdbde-54dd-498b-aca3-132874cfe4a7"
	pageTitle="Scoping Questions for Databricks Job Issue"
	description="Scoping Questions for Databricks Job Issue"
	authors="lisaliu"
	ms.author="lisaliu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32677701, 32677702, 32677703, 32677704"
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_AzureDatabricks"
/>
# Databricks Cluster Job Issue
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
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
            "id": "is_new_problem",
            "order": 3,
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
            "id": "job_url",
            "order": 150,
            "controlType": "textbox",
            "displayLabel": "Job URL for the job with issue",
            "infoBalloonText": "Follow <a href='https://docs.microsoft.com/azure/databricks/workspace/workspace-details#job-url-and-id'>this article</a> to get Job URL",
            "required": false
        },
        {
            "id": "job_url_goodrun",
            "order": 170,
            "controlType": "textbox",
            "displayLabel": "Job URL from last known good run if available",
            "infoBalloonText": "Follow <a href='https://docs.microsoft.com/azure/databricks/workspace/workspace-details#job-url-and-id'>this article</a> to get Job URL",
            "required": false
        },
        {
            "id": "storage_url",
            "order": 200,
            "controlType": "textbox",
            "displayLabel": "Azure storage account resource ID if job involves reading from or writing to Azure storage account",
            "infoBalloonText": "Get Azure storage account resourcre ID from the Azure Portal under the properties page for the storage account",
            "watermarkText": "Storage account resource ID in the form of /subscriptions/[subscriptionID]/resourceGroups/[resourcegroupname]/providers/Microsoft.Storage/storageAccounts/[storageaccountname]",
            "required": false
        },
        {
            "id": "cluster_url",
            "order": 300,
            "controlType": "textbox",
            "displayLabel": "Cluster URL in case job URL is not available",
            "infoBalloonText": "Follow this <a href='https://docs.microsoft.com/azure/databricks/workspace/workspace-details#cluster-url-and-id'>article</a> to get Cluster URL",
            "required": true
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
