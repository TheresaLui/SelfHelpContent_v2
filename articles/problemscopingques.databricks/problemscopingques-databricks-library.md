<properties
	articleId="1eb7e261-b70e-412d-b3f7-a813b72d4c28"
	pageTitle="Scoping Questions for Databricks Library Issue"
	description="Scoping Questions for Databricks Library Issue"
	authors="lisaliu"
	ms.author="lisaliu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32677656, 32677698, 32677699, 32677700, 32677707"
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_AzureDatabricks"
/>
# Databricks Cluster Library Issue
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Azure Databricks Library Issue",
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
            "id": "install_mechanism",
            "order": 130,
            "controlType": "dropdown",
            "displayLabel": "Installation mechanism",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Init script",
                    "text": "Init script"
                },
                {
                    "value": "UI",
                    "text": "UI"
                },
                {
                    "value": "REST API",
                    "text": "REST API"
                },
                {
                    "value": "Conda",
                    "text": "Conda"
                }
            ],
            "required": false
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
            "id": "job_rul",
            "order": 400,
            "controlType": "textbox",
            "displayLabel": "Job URL if available",
            "infoBalloonText": "Follow <a href='https://docs.azuredatabricks.net/user-guide/faq/workspace-details.html'>this article</a> to get Job URL",
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
