<properties
    pageTitle="Azure Quantum Quota"
    description="Azure Quantum Quota"
    authors="dasto"
    ms.author="dasto"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32784416 "
    productPesIds="15621"
    cloudEnvironments="public"
    schemaVersion="1"
    articleId="problemscopingques-quantum-quota"
    ownershipId="Azure_Quantum"
/>
# Azure Quantum Quota - quotaRequestVersion 1 needs to be added
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Azure Quantum"
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "quota_subtype",
            "order": 2,
            "controlType": "radioButtonGroup",
            "displayLabel": "Choose the type of quota you are requesting",
            "includeInQuotaSummary": true,
            "watermarkText": null,
            "required": "true",
            "filter": false,
            "radioButtonOptions": [
                {
                    "text": "Provider Quota (concurrent jobs, job hours, etc.)",
                    "value": "provider-quota"
                },
                {
                    "text": "Workspace Quota (regional or subscription-level)",
                    "value": "workspace-quota"
                }
            ]
        },
        {
            "id": "quota_workspace_sublevel",
            "visibility": "quota_subtype == workspace-quota",
            "order": 3,
            "controlType": "radioButtonGroup",
            "displayLabel":"Are you requesting an increase to the number of workspaces in an Azure region or at a subscription level?",
            "includeInQuotaSummary": true,
            "watermarkText":"Choose the level that you are requesting quota for - need to includeInQuotaSummary",
            "required": true,
            "radioButtonOptions": [
                {
                    "value": "sub",
                    "text": "Subscription"
                },
                {
                    "value": "region",
                    "text": "Region"
                }
            ]
        },
        {
            "id": "quota_workspace_region",
            "visibility": "quota_subtype == workspace-quota && quota_workspace_sublevel == region",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel":"Azure Region",
            "includeInQuotaSummary": true,
            "watermarkText":"Choose a location - need to includeInQuotaSummary",
            "required": true,
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionId}/locations?api-version=2019-06-01",
                "jTokenPath":"value",
                "textProperty":"displayName",
                "ValueProperty":"name",
                "valuePropertyRegex": ".*",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other"
                }
            }
        },
        {
            "id": "quota_workspace_region_fallback",
            "visibility": "quota_workspace_region == dont_know_answer",
            "order": 5,
            "controlType": "textbox",
            "displayLabel":"Azure Region",
            "includeInQuotaSummary": true,
            "watermarkText":"Specify the region that you are requesting quota for.",
            "required": true
        },
        {
            "id": "quota_workspace_new_limit",
            "visibility": "quota_subtype == workspace-quota && quota_workspace_sublevel != null",
            "order": 6,
            "controlType": "numerictextbox",
            "displayLabel": "New quota value requested",
            "isNewQuotaLimit": true,
            "includeInQuotaSummary": true,
            "watermarkText": "Please specify what number you would like the specified quota type raised to.",
            "required": true,
            "validations": [
                {
                    "type": "GreaterThan",
                    "value": 0
                },
                {
                    "type": "RegExMatch",
                    "value": "^[^.]*$",
                    "text": "Integers only."
                }
            ]
        },
        {
            "id": "quota_workspace_business_justification",
            "visibility": "quota_workspace_new_limit != null",
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "Describe the business requirement",
            "includeInQuotaSummary": true,
            "watermarkText": "Provide business justification for your request",
            "required": false
        },
        {
            "id": "quota_provider_name",
            "visibility": "quota_subtype == provider-quota",
            "order": 8,
            "controlType": "dropdown",
            "displayLabel":"Provider Name",
            "watermarkText":"Choose the provider that you are requesting quota for",
            "includeInQuotaSummary": true,
            "required": true,
            "dropdownOptions": [{
                    "value": "1Qloud",
                    "text": "1Qloud Optimization Platform"
                }, {
                    "value": "Honeywell",
                    "text": "Honeywell Quantum Solutions"
                }, {
                    "value": "IonQ",
                    "text": "IonQ"
                }, {
                    "value": "MS Quantum",
                    "text": "Microsoft Quantum Solutions"
                }, {
                    "value": "Quantum Circuits",
                    "text": "Quantum Circuits, Inc."
                },
                {
                    "value": "dont_know_answer",
                    "text": "Not Sure / Not Listed"
                }
            ]
        },
        {
            "id": "quota_provider_workspace",
            "visibility": "quota_subtype == provider-quota && quota_provider_name != null",
            "order": 9,
            "controlType": "dropdown",
            "displayLabel":"Workspace Name",
            "includeInQuotaSummary": true,
            "watermarkText":"Choose a workspace",
            "required": true,
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionId}/providers/Microsoft.Quantum/workspaces?api-version=2019-11-04-preview",
                "jTokenPath":"value",
                "textProperty":"name, location",
                "textTemplate":"{name}",
                "ValueProperty":"id",
                "valuePropertyRegex": ".*",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other"
                }
            }
        },
        {
            "id": "quota_provider_type",
            "visibility": "quota_subtype == provider-quota && quota_provider_workspace != null && quota_provider_name != dont_know_answer",
            "order": 10,
            "controlType": "radioButtonGroup",
            "displayLabel":"Provider Quota Type",
            "includeInQuotaSummary": true,
            "watermarkText":"Choose the increase that you are requesting for the chosen provider in the chosen workspace",
            "required": true,
            "radioButtonOptions": [{
                    "value": "job-hours",
                    "text": "Monthly Job Hours"
                }, {
                    "value": "job-executions",
                    "text": "Monthly Jobs"
                }, {
                    "value": "concurrent-jobs",
                    "text": "Concurrently executing jobs"
                }
            ]
        },
        {
            "id": "quota_provider_type_fallback",
            "visibility": "quota_subtype == provider-quota && quota_provider_workspace != null && quota_provider_name == dont_know_answer",
            "order": 11,
            "controlType": "textbox",
            "displayLabel":"Provider Quota Type",
            "includeInQuotaSummary": true,
            "watermarkText":"Specify the type of provider quota you'd like to request. For example: Concurrent Jobs",
            "required": true
        },
        {
            "id": "quota_provider_new_limit",
            "visibility": "quota_subtype == provider-quota && quota_provider_workspace != null && quota_provider_workspace != dont_know_answer && quota_provider_name != dont_know_answer",
            "order": 12,
            "controlType": "numerictextbox",
            "displayLabel": "New quota value requested",
            "includeInQuotaSummary": true,
            "isNewQuotaLimit": true,
            "watermarkText": "Please specify what number you would like the specified quota type raised to.",
            "required": true,
            "validations": [
                {
                    "type": "GreaterThan",
                    "value": 0
                },
                {
                    "type": "RegExMatch",
                    "value": "^[^.]*$",
                    "text": "Integers only."
                }
            ]
        },
        {
            "id": "quota_provider_business_justification",
            "visibility": "quota_provider_new_limit != null",
            "order": 13,
            "controlType": "multilinetextbox",
            "displayLabel": "Describe the business requirement",
            "includeInQuotaSummary": true,
            "watermarkText": "Provide business justification for your request",
            "required": false
        },
        {
            "id": "quota_provider_description_fallback",
            "visibility": "quota_provider_workspace == dont_know_answer || quota_provider_name == dont_know_answer",
            "order": 14,
            "controlType": "multilinetextbox",
            "displayLabel": "Describe your quota request",
            "includeInQuotaSummary": true,
            "useAsAdditionalDetails": true,
            "watermarkText": "Provide additional information about your issue, include details such as workspace name, region, type of limit, current value and new value requested as applicable.",
            "required": true
        }
    ]
}
---
