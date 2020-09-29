<properties
    articleId="problemscopingques-application"
    pageTitle="Azure Batch - Application details"
    description="Azure Batch - Application details"
    authors="matthchr"
    ms.author="matthchr"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32635050"
    productPesIds="15614"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
	ownershipId="Compute_AzureBatch"
/>
# Application details
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Application details",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "application_selection",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Select the application that has the problem",
            "watermarkText": "Choose an application",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionId}/resourceGroups/{resourcegroup}/providers/Microsoft.Batch/batchAccounts/{resourceName}/applications?api-version=2018-12-01",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Not applicable / Don't know / Resource deleted (include ID in description below)"
                }
            },
            "required": true
        },
        {
            "id": "job_id_selection",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Provide the application version if applicable",
            "watermarkText": "The application version",
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
