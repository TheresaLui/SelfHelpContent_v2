<properties
	articleId="a0cf70ba-6b43-43fa-9806-3fa329592dde"
	pageTitle="Scoping Questions for ADLA Job started to fail with error"
	description="Scoping Questions for ADLA Job start to fail with error"
	authors="guyhay, lisaliu"
	ms.author="guyhay, lisaliu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32680650"
	productPesIds="15940"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_AzureDataLakeAnalytics"
/>
# ADLA Job started to fail with error
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "ADLA Job started to fail with error",
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
            "id": "adla_account_name",
            "order": 130,
            "controlType": "textbox",
            "displayLabel": "ADLA account name",
            "watermarkText": "Please provide the Azure Data Lake Analytics Account name",
            "required": true
        },
        {
            "id": "failed_job_name",
            "order": 140,
            "controlType": "textbox",
            "displayLabel": "Failed job name",
            "watermarkText": "Please provide the job name for the job that failed",
            "required": false
        },
        {
            "id": "failed_job_url",
            "order": 150,
            "controlType": "textbox",
            "displayLabel": "Failed job URL",
            "watermarkText": "Please provide the job URL for the job that failed",
            "required": false
        },
        {
            "id": "successful_job_url",
            "order": 160,
            "controlType": "textbox",
            "displayLabel": "Prior successful job URL",
            "watermarkText": "Please provide the job URL for a previous job that succeeded",
            "required": false
        },
        {
            "id": "usql_script",
            "order": 170,
            "controlType": "multilinetextbox",
            "displayLabel": "U-SQL script",
            "watermarkText": "Please provide the U-SQL script for the job that failed",
            "required": false
        },
        {
            "id": "permission_review_job",
            "order": 200,
            "controlType": "dropdown",
            "displayLabel": "Grant permission to look at the job?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "yes",
                    "text": "Yes, we grant permission to look at the job"
                },
                {
                    "value": "no",
                    "text": "No, we do not grant permission to look at the job"
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
            "order": 500,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional details about the issue",
            "watermarkText": "Please provide the detailed symptoms including the full error message text if available, job graph for both the failed and previous sucessful job, and any other relevant information",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
