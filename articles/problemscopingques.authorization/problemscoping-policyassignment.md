<properties
    pageTitle="Policy behavior not as expected"
    description="Policy behavior not as expected"
    service="microsoft.authorization"
    resource="policyAssignments"
    authors="robga"
    ms.author="robga"
    displayOrder=""
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32739632,32739634,32739635"
    resourceTags=""
    productPesIds="16456"
    cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
    articleId="1d0baad2-c201-4369-9513-233dfa2b6b6b"
    schemaVersion="1"
    ownershipId="Compute_AzurePolicy"
/>
# Policy behavior not as expected
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Policy definition",
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
            "id": "customPolicyDefinition",
            "order": 20,
            "controlType": "dropdown",
            "displayLabel": "Select the policy definition (if it's a custom policy)",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionid}/providers/Microsoft.Authorization/policyDefinitions?api-version=2019-09-01&$filter=policyType eq 'custom'",
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
                    "value": "NoPolicyDefinition",
                    "text": "Unable to retrieve list of policy definition"
                }
            ],
            "required": false
        },
        {
            "id": "builtinPolicyDefinition",
            "order": 30,
            "controlType": "dropdown",
            "displayLabel": "Select the policy definition (if it's a builtin policy)",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionid}/providers/Microsoft.Authorization/policyDefinitions?api-version=2019-09-01&$filter=policyType eq 'builtin'",
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
                    "value": "NoPolicyDefinition",
                    "text": "Unable to retrieve list of policy definition"
                }
            ],
            "required": false
        },
        {
            "id": "policyAssignment",
            "order": 40,
            "controlType": "dropdown",
            "displayLabel": "Select the policy assignment",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionid}/providers/Microsoft.Authorization/policyAssignments?api-version=2019-01-01&$filter=atScope()",
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
                    "value": "NoPolicyAssignment",
                    "text": "Unable to retrieve list of policy assignment"
                }
            ],
            "required": true
        },
        {
            "id": "problem_description",
            "order": 50,
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
