<properties
    pageTitle="Azure Quantum Quota"
    description="Azure Quantum Quota"
    authors="dasto"
    ms.author="dasto"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32740176"
    productPesIds="17040"
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
    "title": "Azure Quantum",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start? - TO BE DELETED",
            "infoBalloonText": "Enter the approximate time you started to see the error.",
            "required": true
        },
        {
            "id": "quota_subtype",
            "order": 2,
            "controlType": "radioButtonGroup",
            "displayLabel": "Choose the type of quota you are requesting - need to includeInQuotaSummary",
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
            "id": "quota_provider",
            "visibility": "quota_subtype == provider-quota",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel":"Provider Name",
            "watermarkText":"Choose the provider that you are requesting quota for - need to includeInQuotaSummary",
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
            "id": "quota_sublevel",
            "visibility": "quota_subtype == workspace-quota",
            "order": 4,
            "controlType": "radioButtonGroup",
            "displayLabel":"Are you requesting an increase to the number of workspaces in an Azure region or at a subscription level?",
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
            "id": "quota_workspace",
            "visibility": "quota_subtype == provider-quota && quota_provider != null",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel":"Workspace Name",
            "watermarkText":"Choose a workspace - need to includeInQuotaSummary",
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
            "id": "quota_region",
            "visibility": "quota_subtype == workspace-quota && quota_sublevel == region",
            "order": 6,
            "controlType": "dropdown",
            "displayLabel":"Azure Region",
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
            "id": "quota_provider_type",
            "visibility": "quota_subtype == provider-quota && quota_workspace != null",
            "order": 7,
            "controlType": "radioButtonGroup",
            "displayLabel":"Provider Quota Type",
            "watermarkText":"Choose the increase that you are requesting for the chosen provider in the chosen workspace - need to includeInQuotaSummary",
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
            "id": "quota_new_limit",
            "order": 8,
            "controlType": "numerictextbox",
            "displayLabel": "New quota value requested isNewQuotaLimit eqs true",
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
            "id": "business_justification",
            "visibility": "(quota_new_limit != null && quota_region != dont_know_answer) || (quota_new_limit != null && quota_workspace != dont_know_answer)",
            "order": 9,
            "controlType": "multilinetextbox",
            "displayLabel": "Describe the business requirement",
            "watermarkText": "Provide business justification for your request",
            "required": false
        },
        {
            "id": "problem_description_fallback",
            "visibility": "quota_region == dont_know_answer || quota_workspace == dont_know_answer || quota_provider == dont_know_answer",
            "order": 10,
            "controlType": "multilinetextbox",
            "displayLabel": "Describe your quota request - need to useAsAdditionalDetails",
            "watermarkText": "Provide additional information about your issue, include details such as account name, type of limit, current value and new value requested.",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Description - TO BE DELETED",
            "required": true,
            "useAsAdditionalDetails": true,
            "watermarkText": "Provide additional information about your issue. If available, please include the full error message and any stack traces you are receiving."
        }
    ]
}
---
