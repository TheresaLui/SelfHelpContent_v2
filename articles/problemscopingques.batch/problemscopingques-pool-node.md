<properties
    articleId="problemscopingques-pool-node"
    pageTitle="Azure Batch - Pool and node details"
    description="Azure Batch - Pool and node details"
    authors="matthchr"
    ms.author="matthchr"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32635093,32635082,32635066,32635079"
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
    "title": "Pool and node details",
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
            "id": "vm_id_selection",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Provide the Batch Node ID which has the problem",
            "watermarkText": "The Batch Node ID which has the problem",
            "required": true
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
