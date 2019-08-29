<properties
	articleId="cb6e882e-5a9a-42e7-aff0-3354c6e8dd7c"
	pageTitle="Scoping Questions for ADLA Job Submission Errors"
	description="Scoping Questions for ADLA Job Submission Errors"
	authors="guyhay, lisaliu, v-anukar"
	ms.author="guyhay, lisaliu, v-anukar"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32680648"
	productPesIds="15940"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# ADLA Job Submission Errors
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "ADLA Job Submission Errors",
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
            "id": "request_id",
            "order": 140,
            "controlType": "textbox",
            "displayLabel": "Request ID in CloudException",
            "watermarkText": "Please provide the requestID/operationID in the cloud exception",
            "required": true
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
            "required": false,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
