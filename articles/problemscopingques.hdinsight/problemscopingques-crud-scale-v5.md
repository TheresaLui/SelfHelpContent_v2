<properties
	articleId="2891e506-230d-4cb2-b45f-149ec6d000b8"
	pageTitle="Scoping Questions for HDInsight Scaling Issue"
	description="Scoping Questions for HDInsight Scaling Issue"
	authors="shravanmn, csunilkumar, lisaliu"
	ms.author="shravan, sunilkc, lisaliu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32681540, 32681539, 32681538"
	productPesIds="15078"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_HDInsight"
/>
# HDI Cluster Scaling Issue
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "HDInsight CRUD Issue",
    "fileAttachmentHint": "Please provide the ARM template and the exact command used for the CRUD operation, if applicable",
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
            "order": 50,
            "controlType": "dropdown",
            "displayLabel": "Is this a new problem, or the problem has happened before?",
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
            "required": false
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
            "id": "CRUD_request_submission_method",
            "order": 200,
            "controlType": "dropdown",
            "displayLabel": "How was the scaling request submitted?",
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
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "clusterID",
            "order": 300,
            "controlType": "dropdown",
            "displayLabel": "Cluster ID if the cluster is still running",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionid}/resourceGroups/{resourcegroup}/providers/Microsoft.HDInsight/clusters/{resourcename}?api-version=2018-06-01-preview",
                "jTokenPath": "properties", 
                "textProperty": "clusterId",
                "valueProperty": "clusterId",
                "textPropertyRegex": "[^/]+$",
                "valuePropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "Cluster ID not available",
                    "text": "Cluster ID not available"
                }
            },
            "required": false
        },
        {
            "id": "problem_description",
            "order": 500,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional details about the issue",
            "watermarkText": "Please provide the detail symptom including the full error text if available, whether the issue is intermittent or persistent, and any other relevant information",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
