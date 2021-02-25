<properties
    pageTitle="Issues related to Policy Exemptions"
    description="Issues related to Policy Exemptions"
    service="microsoft.authorization"
    resource="remediations"
    authors="kenieva"
    ms.author="kenieva"
    displayOrder=""
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32758299"
    resourceTags=""
    productPesIds="16456"
    cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
    articleId="1d0baad2-c201-4369-9513-233dfa2b6b99"
    schemaVersion="1"
    ownershipId="Compute_AzurePolicy"
/>
# Issues related to Policy Exemptions
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Policy Exemption",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 10,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "policyExemption",
            "order": 20,
            "controlType": "dropdown",
            "displayLabel": "Select the policy exemption",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionid}/providers/Microsoft.Authorization/policyExemptions?api-version=2020-07-01-preview",
                "jTokenPath": "value",
                "textProperty": "properties.displayName,id",
                "textTemplate": "{properties.displayName}  ({id})",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            },
            "DropdownOptions": [
                {
                    "value": "NoPolicyExemption",
                    "text": "Unable to retrieve list of policy exemptions"
                }
            ],
            "required": true
        },
        {
            "id": "problem_description",
            "order": 30,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Provide additional information about the issue and what is your expectation",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Issue description."
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---
