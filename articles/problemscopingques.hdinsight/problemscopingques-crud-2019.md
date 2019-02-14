<properties
	articleId="8d11697c-66b9-4de9-a1dd-c6b6d05cad4b"
	pageTitle="Scoping Questions for HDInsight CRUD Issue"
	description="Scoping Questions for HDInsight CRUD Issue"
	authors="lisaliu"
	ms.author="lisaliu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32628987, 32629002, 32629004, 32629016, 32629032, 32629036, 32629037, 32629084, 32629125, 32629129, 32629157, 32629158, 32629159, 32629160"
	productPesIds="15078"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# CRUD Issue
---
{
    "resourceRequired": true,
    "title": "HDInsight CRUD Issue",
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
                    "text": "Happened before"
                }
            ],
            "required": true
        },
        {
            "id": "is_vnet_peering",
            "order": 150,
            "controlType": "dropdown",
            "displayLabel": "Is VNET peering involved?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                }
            ],
            "required": true
        },
        {
            "id": "CRUD_request_submission_method",
            "order": 200,
            "controlType": "dropdown",
            "displayLabel": "How was the CRUD request submitted?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Azure Portal",
                    "text": "Azure Portal"
                },
                {
                    "value": "ARM Template",
                    "text": "ARM Template"
                },
                {
                    "value": "Azure CLI",
                    "text": "Azure CLI"
                },
                {
                    "value": "Power Shell",
                    "text": "Power Shell"
                },
                {
                    "value": "Azure Data Factory Activity",
                    "text": "Azure Data Factory Activity"
                },
                {
                    "value": "Azure Automation runbook",
                    "text": "Azure Automation runbook"
                },
                {
                    "value": "Other (describe below)",
                    "text": "Other"
                }
            ],
            "required": true
        },
        {
            "id": "user_agent",
            "order": 300,
            "controlType": "dropdown",
            "displayLabel": "What is the browser being used?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Edge",
                    "text": "Edge"
                },
                {
                    "value": "Internet Explorer",
                    "text": "Internet Explorer"
                },
                {
                    "value": "Google Chrome",
                    "text": "Google Chrome"
                },
                {
                    "value": "Firefox",
                    "text": "Firefox"
                },
                {
                    "value": "Other (describe below)",
                    "text": "Other"
                }
            ],
            "required": true
        },
        {
            "id": "problem_description",
            "order": 500,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional details about the issue",
            "watermarkText": "Please provide the detail symptom including the full error text if available, whether the issue is intermittent or persistent, and any other relevant information",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "learn_more_text",
            "order": 600,
            "controlType": "infoblock",
            "content": "<a href='https://hdinsight.github.io/ClusterCRUD/clustercrud-landing'>Learn more</a> about commonly faced issues with using Spark on HDInsight"
        }
    ]
}
---
