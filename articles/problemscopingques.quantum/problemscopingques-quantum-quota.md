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
# Azure Quantum Quota
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Azure Quantum",
    "fileAttachmentHint": "",
    "quotaRequestVersion": "1.0",
    "formElements": [
        {
            "id": "quota_subtype",
            "order": 1,
            "controlType": "radioButtonGroup",
            "displayLabel": "Choose the type of quota you are requesting",
            "watermarkText": null,
            "required": "true",
            "filter": false,
            "includeInQuotaSummary": true,
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
            "order": 2,
            "controlType": "dropdown",
            "displayLabel":"Provider Name",
            "watermarkText":"Choose the provider that you are requesting quota for",
            "required": true,
            "includeInQuotaSummary": true,
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
                }
            ]
        },
        {
            "id": "quota_sublevel",
            "visibility": "quota_subtype == workspace-quota",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel":"Are you requesting an increase to the number of workspaces in an Azure region or at a subscription level?",
            "watermarkText":"Choose the level that you are requesting quota for",
            "required": true,
            "includeInQuotaSummary": true,
            "dropdownOptions": [
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
            "visibility": "quota_subtype == provider-quota",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel":"Workspace Name",
            "watermarkText":"Choose a workspace",
            "required": true,
            "includeInQuotaSummary": true,
            "dynamicDropdownOptions": {
                "dependsOn": "quota_subtype",
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
            "visibility": "quota_subtype == workspace-quota && quota_sublevel == sub",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel":"Azure Region",
            "watermarkText":"Choose a location",
            "required": true,
            "includeInQuotaSummary": true,
            "dynamicDropdownOptions": {
                "dependsOn": "quota_subtype",
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
            "visibility": "quota_subtype == provider-quota",
            "order": 6,
            "controlType": "dropdown",
            "displayLabel":"Provider Quota Type",
            "watermarkText":"Choose the increase that you are requesting for the chosen provider in the chosen workspace",
            "required": true,
            "includeInQuotaSummary": true,
            "dropdownOptions": [{
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
            "id": "new_limit",
            "visibility": "quota_subtype == workspace-quota ||  quota_subtype == provider-quota",
            "order": 7,
            "controlType": "numerictextbox",
            "displayLabel": "New quota requested",
            "infoBalloonText": "Put the new value for the limit you are requesting here.",
            "required": true,
            "validations": [
                {
                    "type": "greaterthan",
                    "value": 0
                }
                ],
            "isNewQuotaLimit": true
        },
        {
            "id": "business_justification",
            "visibility": "quota_subtype != null && quota_region != dont_know_answer && quota_workspace != dont_know_answer",
            "order": 8,
            "controlType": "multilinetextbox",
            "displayLabel": "Describe the business requirement",
            "watermarkText": "Provide business justification for your request",
            "required": false
        },
        {
            "id": "problem_description",
            "visibility": "quota_subtype != null && quota_region == dont_know_answer || quota_workspace == dont_know_answer",
            "order": 9,
            "controlType": "multilinetextbox",
            "displayLabel": "Describe your quota request",
            "watermarkText": "Provide additional information about your issue, include details such as account name, type of limit, current value and new value requested.",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ]
}
---
