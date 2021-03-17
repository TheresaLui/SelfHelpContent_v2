<properties
	articleId="6b0e2f04-209b-487f-98c1-fc0306b87f57"
	pageTitle="Scoping Questions for Databricks Spark Issue"
	description="Scoping Questions for Databricks Spark Issue"
	authors="lisaliu"
	ms.author="lisaliu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32677724, 32677725, 32677727, 32681393"
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_AzureDatabricks"
/>
# Databricks Cluster Spark Issue
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Azure Databricks Spark Issue",
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
            "id": "is_previous_dbr_working",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Was it working in previous DBR?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "yes",
                    "text": "yes"
                },
                {
                    "value": "no",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "previous_dbr_version",
            "visibility": "is_previous_dbr_working == yes",
            "order": 110,
            "controlType": "textbox",
            "displayLabel": "Previous DBR version if available",
            "watermarkText": "If it was working in previous DBR, please provide previous DBR version",
            "required": false
        },
        {
            "id": "notebook_rul",
            "order": 300,
            "controlType": "textbox",
            "displayLabel": "Notebook URL if available",
            "infoBalloonText": "Follow <a href='https://docs.microsoft.com/azure/databricks/workspace/workspace-details#--notebook-url-and-id'>this article</a> to get Notebook URL",
            "required": false
        },
        {
            "id": "cluster_url",
            "order": 170,
            "controlType": "textbox",
            "displayLabel": "Cluster URL if notebook URL is not available",
            "infoBalloonText": "Follow this <a href='https://docs.microsoft.com/azure/databricks/workspace/workspace-details#cluster-url-and-id'>article</a> to get Cluster URL",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 600,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional details about the issue",
            "watermarkText": "Please provide the detail symptom including the full error text, result in the Notebook cell, what task was being performed when the issue occurred, whether the issue is intermittent or persistent, and any other relevant information",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
