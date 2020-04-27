<properties
    articleId="problemscopingques-job-task"
    pageTitle="Azure Batch - Job details"
    description="Azure Batch - Job details"
    authors="matthchr"
    ms.author="matthchr"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32635073,32635070,32635089,32635088,32635087,32635076,32635092,32635078"
    productPesIds="15614"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
	ownershipId="Compute_AzureBatch"
/>
# Job and task details
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Job and task details",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "job_id_selection",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Provide the job ID which has the problem",
            "watermarkText": "The job ID which has the problem",
            "required": true
        },
        {
            "id": "task_id_selection",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Provide the task IDs which have the problem",
            "watermarkText": "The task IDs which have the problem",
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 4,
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
