<properties
    pageTitle="MySQL-Quota"
    description="MySQL-Quota"
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
# MySQL Quota Questions
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "MySQL-Quota",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "quotaType",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Quota type",
            "watermarkText": null,
            "required": "true",
            "filter": false,
            "dropdownOptions": [
                {
                    "text": "Region access",
                    "value": "enableregion"
                },
                {
                    "text": "Other",
                    "value": "dont_know_answer"
                }
            ]
        },
        {
            "id": "region_requested",
            "visibility": "quotaType != null && quotaType == enableregion",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel":"Region requested",
            "watermarkText":"Choose a region",
            "required": true,
            "dynamicDropdownOptions": {
                "dependsOn": "quotaType",
                "uri": "/subscriptions/{subscriptionId}/locations?api-version=2019-06-01",
                "jTokenPath":"value",
                "textProperty":"displayName",
                "ValueProperty":"displayName",
                "valuePropertyRegex": ".*",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other"
                }
            }
        },
        {
            "id": "capacity_requested",
            "visibility": "quotaType != null && quotaType == enableregion",
            "order": 3,
            "controlType": "numerictextbox",
            "displayLabel": "Capacity requesed (in VCores)",
            "infoBalloonText": "<a href='https://go.microsoft.com/fwlink/?linkid=867609'>Learn more</a>.",
            "required": true
        },
        {
            "id": "business_justification",
            "visibility": "quotaType != null && quotaType == enableregion",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Describe the business requirement",
            "watermarkText": "Provide business justification for your request",
            "required": false
        },
        {
            "id": "problem_description",
            "visibility": "quotaType != null && quotaType == dont_know_answer",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Describe your quota request",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ]
}
---