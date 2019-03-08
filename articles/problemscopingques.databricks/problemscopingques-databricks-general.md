<properties
	articleId="2535ac26-597f-4894-8797-0e98a2eb6043"
	pageTitle="Scoping Questions for Databricks Issue"
	description="Scoping Questions for Databricks Issue"
	authors="lisaliu"
	ms.author="lisaliu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32612186, 32612187, 32612188, 32612189, 32612190, 32612191, 32612192, 32612193, 32612194, 32612195, 32612196, 32612198, 32612199, 32612200, 32612201, 32612202, 32612203, 32612204, 32612206, 32612207, 32612210"
	productPesIds="16432"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# Databricks Issue
---
{
    "resourceRequired": true,
    "title": "Azure Databricks General Issue",
    "fileAttachmentHint": "Please upload Spark Driver and Executor log if applicable to help expedite the investigation",
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
            "id": "workspace_id",
            "order": 150,
            "controlType": "textbox",
            "displayLabel": "Workspace ID if available",
            "required": true
        },
        {
            "id": "cluster_url",
            "order": 170,
            "controlType": "textbox",
            "displayLabel": "Cluster URL if available",
            "required": true
        },
        {
            "id": "workload_submission_method",
            "order": 200,
            "controlType": "dropdown",
            "displayLabel": "How was the workload submitted?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Notebook",
                    "text": "Notebook"
                },
                {
                    "value": "ADF",
                    "text": "ADF"
                },
                {
                    "value": "RESTAPI",
                    "text": "REST API"
                },
                {
                    "value": "ScheduledJob",
                    "text": "Scheduled job from the UI"
                },
                                {
                    "value": "Other",
                    "text": "Other"
                }
            ],
            "required": true
        },
        {
            "id": "notebook_rul",
            "visibility": "workload_submission_method == Notebook",
            "order": 300,
            "controlType": "textbox",
            "displayLabel": "Notebook URL if available",
            "required": true
        },
        {
            "id": "job_url",
            "visibility": "workload_submission_method != Notebook",
            "order": 400,
            "controlType": "textbox",
            "displayLabel": "Job URL if available",
            "required": true
        },
        {
            "id": "instruction",
            "order": 500,
            "controlType": "infoblock",
            "content": "Follow this <a href='https://docs.azuredatabricks.net/user-guide/faq/workspace-details.html'>article</a> to get the requested Workspace, Cluster, Notebook, and Job information"
        },
        {
            "id": "problem_description",
            "order": 600,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional details about the issue",
            "watermarkText": "Please provide the detail symptom including the full error text, result in the Notebook cell, what task was being performed when the issue occurred, whether the issue is intermittent or persistent, and any other relevant information",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "learn_more_text",
            "order": 700,
            "controlType": "infoblock",
            "content": "<a href='https://docs.microsoft.com/azure/azure-databricks/'>Learn more</a> about Azure Databricks"
        }
    ]
}
---
