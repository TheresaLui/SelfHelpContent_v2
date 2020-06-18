<properties
    articleId="problemscopingques-account-private-endpoint"
    pageTitle="Azure Batch - Batch account and private endpoint details"
    description="Azure Batch - Batch account and private endpoint details"
    authors="pkshultz"
    ms.author="p"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32742951"
    productPesIds="15614"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
	ownershipId="Compute_AzureBatch"
/>
# Batch account and private endpoint details
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Batch account and private endpoint details",
    "fileAttachmentHint": "",
    "formElements": [
     {
            "id": "private_endpoint_id_selection",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Select the private endpoint associated with the Batch account",
            "watermarkText": "Choose a private endpoint",
            "dynamicDropdownOptions": {
				"uri": "/subscriptions/{subscriptionId}/resourceGroups/{resourcegroup}/providers/Microsoft.Network/privateEndpoints?api-version=2020-04-01",
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
