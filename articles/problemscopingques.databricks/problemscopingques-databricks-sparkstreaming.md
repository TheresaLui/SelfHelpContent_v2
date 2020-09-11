<properties
	articleId="2759a82c-f1b2-4d5b-b63a-368dccab4a8b"
	pageTitle="Scoping Questions for Databricks Spark Streaming Issue"
	description="Scoping Questions for Databricks Spark Streaming Issue"
	authors="lisaliu"
	ms.author="lisaliu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32681391, 32681392"
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_AzureDatabricks"
/>
# Databricks Cluster Spark Streaming Issue
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Azure Databricks Spark Streaming Issue",
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
            "id": "job_rul",
            "order": 200,
            "controlType": "textbox",
            "displayLabel": "Job URL for the streaming job with issue",
            "infoBalloonText": "Follow <a href='https://docs.microsoft.com/azure/databricks/workspace/workspace-details#job-url-and-id'>this article</a> to get Job URL",
            "required": false
        },
        {
            "id": "cluster_url",
            "order": 210,
            "controlType": "textbox",
            "displayLabel": "Cluster URL if job URL is not available",
            "infoBalloonText": "Follow this <a href='https://docs.microsoft.com/azure/databricks/workspace/workspace-details#cluster-url-and-id'>article</a> to get Cluster URL",
            "required": false
        },
        {
            "id": "streamingsource",
            "order": 300,
            "controlType": "textbox",
            "displayLabel": "Source of the streaming job",
            "watermarkText": "Please specify the source for the streaming job, such as Azure Blob Storage, Delta, Event Hub",
            "required": true
        },
        {
            "id": "streamingsink",
            "order": 310,
            "controlType": "textbox",
            "displayLabel": "Sink of the streaming",
            "watermarkText": "Please specify the sink for the streaming job, such as Delta, or a Custom sink",
            "required": false
        },
        {
            "id": "stuckorslow",
            "order": 400,
            "controlType": "dropdown",
            "displayLabel": "Is the streaming job stuck or slow",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "stuck",
                    "text": "Stuck"
                },
                {
                    "value": "slow",
                    "text": "Slow"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "problemfrequency",
            "order": 410,
            "controlType": "dropdown",
            "displayLabel": "When would the symptom start?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "immediate",
                    "text": "Immediately after the streaming job started"
                },
                {
                    "value": "afteraperiod",
                    "text": "After the job had run for a period of time"
                },
                {
                    "value": "notconsistent",
                    "text": "Intermittently, could occur any time after the job started"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "statefuloperation",
            "order": 420,
            "controlType": "dropdown",
            "displayLabel": "Any stateful operation such as streaming aggregation is involved",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "yes",
                    "text": "Yes"
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
