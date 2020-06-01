<properties
    pageTitle="Guest Configuration"
    description="Guest Configuration"
    service="microsoft.authorization"
    resource="policyDefinitions"
    authors="kenieva"
    ms.author="kenieva"
    displayOrder=""
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32741669,32741670"
    resourceTags=""
    productPesIds="16456"
    cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
    articleId="1d0baad2-c201-4369-9513-233dfa2b6b6d"
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
            "displayLabel": "Please select the policy definition (if it's a custom policy)",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionid}/providers/Microsoft.Authorization/policyDefinitions?api-version=2019-09-01&$filter=policyType eq 'custom'",
                "jTokenPath": "value",
                "textProperty": "properties.displayName,name",
                "textTemplate": "{properties.displayName}  ({name})",
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
            "displayLabel": "Please select the policy definition (if it's a builtin policy)",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionid}/providers/Microsoft.Authorization/policyDefinitions?api-version=2019-09-01$filter=category eq 'Guest Configuration'",
                "jTokenPath": "value",
                "textProperty": "properties.displayName,name",
                "textTemplate": "{properties.displayName}  ({name})",
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
            "displayLabel": "Please select the policy assignment",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionid}/providers/Microsoft.Authorization/policyAssignments?api-version=2019-01-01&$filter=atScope()",
                "jTokenPath": "value",
                "textProperty": "properties.displayName,name",
                "textTemplate": "{properties.displayName}  ({name})",
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
            "required": false
        },
            {
            "id": "policyInitative",
            "order": 50,
            "controlType": "dropdown",
            "displayLabel": "Please select the policy initative",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionid}/providers/Microsoft.Authorization/policySetDefinitions?api-version=2019-09-01$filter=category eq 'Guest Configuration'",
                "jTokenPath": "value",
                "textProperty": "properties.displayName,name",
                "textTemplate": "{properties.displayName}  ({name})",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            },
            "DropdownOptions": [
                {
                    "value": "NoPolicyInitative",
                    "text": "Unable to retrieve list of policy initative"
                }
            ],
            "required": false
        },
           {
            "id": "VM",
            "order": 60,
            "controlType": "dropdown",
            "displayLabel": "Please select the Virtual Machine",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionid}/providers/Microsoft.Compute/virtualMachines?api-version=2019-12-01",
                "jTokenPath": "value",
                "textProperty": "name",
                "textTemplate": "{name}",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            },
            "DropdownOptions": [
                {
                    "value": "NoVM",
                    "text": "Unable to retrieve list of virtual machines"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 70,
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
