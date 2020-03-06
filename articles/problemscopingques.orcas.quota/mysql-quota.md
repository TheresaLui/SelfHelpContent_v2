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
    "fileAttachmentHint": "Please upload file to support your request",
    "formElements": [
        {
            "id": "region_requested",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel":"Region requested",
            "watermarkText":"Choose a region",
            "required": true,
            "dynamicDropdownOptions": {
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
            "order": 2,
            "controlType": "numerictextbox",
            "displayLabel": "Capacity requesed (in VCores)",
            "infoBalloonText": "<a href='https://docs.microsoft.com/en-us/azure/mysql/concepts-pricing-tiers'>Learn more</a>.",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Describe the business requirement",
            "watermarkText": "Provide business justification for your request",
            "required": false,
            "useAsAdditionalDetails": true
        }
    ]
}
---