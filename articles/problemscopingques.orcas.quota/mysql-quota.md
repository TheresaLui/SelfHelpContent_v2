<properties
    pageTitle="MySql-Quota"
    description="MySql-Quota"
    authors="ambrahma"
    ms.author="ambrahma"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32684016"
    productPesIds="15621"
    cloudEnvironments="Public, Fairfax"
    schemaVersion="1"
    articleId="problemscopingques-orcas-quota-mysql"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>
# MySql Quota Questions
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "MySql-Quota",
    "fileAttachmentHint": "Please upload your file to support your request",
    "formElements": [
        {
            "id": "quotaSubType",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Quota Sub-type",
            "watermarkText": "Choose an option",
            "required": "true",
            "dropdownOptions": [
                {
                    "text": "MySQL region enable",
                    "value": "enableregion"
                },
                {
                    "text": "Others",
                    "value": "dont_know_answer"
                }
            ]
        },
        {
            "id": "location",
            "visibility": "quotaSubType != null && quotaSubType == enableregion",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel":"Please choose the region in which you want to have MySQL Server",
            "watermarkText":"Choose a region",
            "required": true,
            "dynamicDropdownOptions": {
                "dependsOn": "quotaSubType",
                "uri": "/subscriptions/{subscriptionId}/locations?api-version=2019-06-01",
                "jTokenPath":"value",
                "textProperty":"displayName",
                "ValueProperty":"displayName",
                "valuePropertyRegex": ".*",
                "defaultDropdownOptions": {
                "value": "dont_know_answer",
                "text": "Other, don't know or not applicable"
                }
            }
        },
        {
            "id": "capacity_requested",
            "visibility": "quotaSubType != null && quotaSubType == enableregion",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Please provide specific capacity for your request",
            "watermarkText": "For example, 30 General purpose vCores",
            "required": false
        },
        {
            "id": "problem_description",
            "visibility": true,
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Describe your quota request",
            "watermarkText": "Provide additional information about your issue",
            "required": false,
            "useAsAdditionalDetails": true
        }
    ]
}
---