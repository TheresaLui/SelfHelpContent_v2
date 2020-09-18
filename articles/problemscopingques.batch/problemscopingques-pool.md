<properties
    articleId="problemscopingques-pool"
    pageTitle="Azure Batch - Pool details"
    description="Azure Batch - Pool details"
    authors="matthchr"
    ms.author="matthchr"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32635069,32635072,32635061,32635091,32635094,32635065,32635053"
    productPesIds="15614"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
	ownershipId="Compute_AzureBatch"
/>
# Pool details
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Pool details",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "pool_id_selection",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Select the pool that has the problem",
            "watermarkText": "Choose a pool",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionId}/resourceGroups/{resourcegroup}/providers/Microsoft.Batch/batchAccounts/{resourceName}/pools?api-version=2018-12-01",
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
