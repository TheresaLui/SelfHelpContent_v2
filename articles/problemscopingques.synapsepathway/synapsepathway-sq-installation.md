<properties
    schemaVersion = "1"
    selfHelpType = "problemScopingQuestions"
    cloudEnvironments = "public, fairfax, blackforest, mooncake, usnat, ussec"
    ownershipId = "AzureData_SynapseAnalytics"
    productPesIds = "17487"
    supportTopicIds = "32788656"
    pageTitle = "Installation"
    description = "Installation"
    articleId = "synapsepathway-sq-installation.md"
    ms.author = "goventur"
/>

# Installation

---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": false,
    "resourceRequired": false,
    "fileAttachmentHint": "",
    "title": "Installation",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "required": true,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start",
            "infoBalloonText": ""
        },
        {
            "id": "is_reproducible",
            "order": 2,
            "required": false,
            "controlType": "radioButtonGroup",
            "displayLabel": "Is the problem reproducible?",
            "radioButtonOptions": [{
                    "value": "Yes",
                    "text": "Yes"
                }, {
                    "value": "No",
                    "text": "No"
                }
            ]
        },
        {
            "id": "problem_description",
            "order": 3,
            "required": true,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue (include error message and steps to reproduce, if applicable)",
            "infoBalloonText": "",
            "useAsAdditionalDetails": true
        }
    ]
}
---



