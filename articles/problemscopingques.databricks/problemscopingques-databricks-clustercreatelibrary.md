<properties
	articleId="c06430f0-945f-482d-bc36-b33586596b84"
	pageTitle="Scoping Questions for Databricks Cluster Create failure involving library"
	description="Scoping Questions for Databricks Cluster Create failure involving library"
	authors="lisaliu"
	ms.author="lisaliu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32677679"
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_AzureDatabricks"
/>
# Databricks Cluster Creation Termination Sizing Issue
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Azure Databricks Cluster Creationg Termination Sizing Issue",
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
            "id": "howinstalled",
            "order": 70,
            "controlType": "dropdown",
            "displayLabel": "How the library is being installed?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "initscript",
                    "text": "Init script"
                },
                {
                    "value": "libraryui",
                    "text": "Library UI"
                },
                {
                    "value": "notebook",
                    "text": "Notebook"
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
            "infoBalloonText": "Follow this <a href='https://docs.azuredatabricks.net/user-guide/faq/workspace-details.html'>article</a> to get Cluster URL",
            "required": true
        },
        {
            "id": "workspace_id",
            "order": 170,
            "controlType": "textbox",
            "displayLabel": "Workspace ID if cluster URL is not available",
            "infoBalloonText": "Follow this <a href='https://docs.azuredatabricks.net/user-guide/faq/workspace-details.html'>article</a> to get Workspace ID",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 600,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional details about the issue",
            "watermarkText": "Please provide additional details about the issue, such as whether the issue is intermittent or persistent, and any other relevant information",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
