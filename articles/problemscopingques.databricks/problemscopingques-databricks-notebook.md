<properties
	articleId="3b41f823-f4a9-4989-93d3-0c6ab45f8435"
	pageTitle="Scoping Questions for Databricks Notebook Issue"
	description="Scoping Questions for Databricks Notebook Issue"
	authors="lisaliu"
	ms.author="lisaliu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32677659, 32677690, 32677693, 32677695, 32677716, 32677728, 32677731"
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_AzureDatabricks"
/>
# Databricks Cluster Notebook Issue
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Azure Databricks Notebook Issue",
    "fileAttachmentHint": "Please attach HAR file from the client machine if the issue is related to responsiveness",
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
            "id": "cluster_url",
            "order": 170,
            "controlType": "textbox",
            "displayLabel": "Cluster URL",
            "infoBalloonText": "Follow this <a href='https://docs.azuredatabricks.net/user-guide/faq/workspace-details.html'>article</a> to get Cluster URL",
            "required": true
        },
        {
            "id": "notebook_rul",
            "order": 300,
            "controlType": "textbox",
            "displayLabel": "Notebook URL if available",
            "infoBalloonText": "Follow <a href='https://docs.azuredatabricks.net/user-guide/faq/workspace-details.html'>this article</a> to get Notebook URL",
            "required": false
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
