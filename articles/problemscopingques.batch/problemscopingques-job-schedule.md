<properties
    articleId="problemscopingques-job-schedule"
    pageTitle="Azure Batch - Job Schedule details"
    description="Azure Batch - Job Schedule details"
    authors="matthchr"
    ms.author="matthchr"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32635075"
    productPesIds="15614"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
	ownershipId="Compute_AzureBatch"
/>
# Job Schedule details
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Job Schedule details",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "job_schedule_id_selection",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Provide the job schedule ID which has the problem",
            "watermarkText": "The job schedule ID which has the problem",
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Provide additional information about your issue."
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---
