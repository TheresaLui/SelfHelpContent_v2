<properties
	articleId="300da47f-593c-4ac6-ae42-fd03befd5d5f"
	pageTitle="Scoping Questions for ADLA job stated to run slow"
	description="Scoping Questions for ADLA job stated to run slow"
	authors="guyhay, lisaliu"
	ms.author="guyhay, lisaliu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32680652"
	productPesIds="15940"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureData_AzureDataLakeAnalytics"
/>
# ADLA job stated to run slow
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "ADLA job stated to run slow",
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
            "id": "job_name",
            "order": 140,
            "controlType": "textbox",
            "displayLabel": "Job name",
            "watermarkText": "Please provide the job name for the job that failed",
            "required": false
        },
        {
            "id": "job_url",
            "order": 150,
            "controlType": "textbox",
            "displayLabel": "Job URL",
            "watermarkText": "Please provide the job URL for the job that failed",
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
            "watermarkText": "Please provide the detail symptom including the full error message text if available, and any other relevant information",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
