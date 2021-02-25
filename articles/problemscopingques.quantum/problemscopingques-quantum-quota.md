<properties
    pageTitle="Azure-Quantum-Quota"
    description="Azure Quantum Quota"
    authors="dasto"
    ms.author="dasto"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32784416"
    productPesIds="15621"
    cloudEnvironments="public, fairfax, usnat, ussec"
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
    "title": "Azure Quantum Quota",
    "fileAttachmentHint": "",
    "quotaRequestVersion": "1.0",
    "formElements": [
        {
            "id": "quota_subtype",
            "order": 1,
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
            "order": 2,
            "controlType": "radioButtonGroup",
            "displayLabel":"Are you requesting an increase to the number of workspaces in an Azure region or at a subscription level?",
            "includeInQuotaSummary": true,
            "watermarkText":"Choose the level that you are requesting quota for",
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
            "id": "quota_region",
            "visibility": "quota_subtype == workspace-quota && quota_workspace_sublevel == region",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel":"Azure Region",
            "includeInQuotaSummary": true,
            "watermarkText":"Choose a location",
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
            "id": "quota_region_fallback",
            "visibility": "quota_region == dont_know_answer",
            "order": 4,
            "controlType": "textbox",
            "displayLabel":"Azure Region",
            "includeInQuotaSummary": true,
            "watermarkText":"Specify the region that you are requesting quota for.",
            "required": true
        },
        {
            "id": "quota_workspace_new_limit",
            "visibility": "quota_subtype == workspace-quota && quota_workspace_sublevel != null",
            "order": 5,
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
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Describe the business requirement",
            "watermarkText": "Provide business justification for your request",
            "required": false
        },
        {
            "id": "quota_provider_name",
            "visibility": "quota_subtype == provider-quota",
            "order": 7,
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
                    "value": "MS-Quantum",
                    "text": "Microsoft Quantum Solutions"
                }, {
                    "value": "QCI",
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
            "visibility": "quota_provider_name == MS-Quantum || quota_provider_name == dont_know_answer",
            "order": 8,
            "controlType": "dropdown",
            "displayLabel":"Workspace name",
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
            "visibility": "quota_subtype == provider-quota && quota_provider_workspace != null && quota_provider_name == MS-Quantum",
            "order": 9,
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
            "id": "quota_provider_type_ionq",
            "visibility": "quota_subtype == provider-quota&& quota_provider_name != MS-Quantum && quota_provider_name == IonQ",
            "order": 10,
            "controlType": "textBlock",
            "displayLabel": "To request a quota/limit increase for your IonQ offer, reach out to IonQ support. Provide details of your subscripton ID, workspace name, and a business justification. The IonQ support team will evaluate your request. https://aka.ms/AQ/IonQ/CustomerSupport"
        },
        {
            "id": "quota_provider_type_honeywell",
            "visibility": "quota_subtype == provider-quota && quota_provider_name != MS-Quantum && quota_provider_name == Honeywell",
            "order": 11,
            "controlType": "textBlock",
            "displayLabel":"To request a quota/limit increase for your Honeywell offer, reach out to Honeywell support. Provide details of your subscripton ID, workspace name, and a business justification. The Honeywell support team will evaluate your request. https://aka.ms/AQ/Honeywell/CustomerSupport"
        },
        {
            "id": "quota_provider_type_qci",
            "visibility": "quota_subtype == provider-quota && quota_provider_name != MS-Quantum && quota_provider_name == QCI",
            "order": 12,
            "controlType": "textBlock",
            "displayLabel":"To request a quota/limit increase for your Quantum Circuits Inc. (QCI) offer, reach out to QCI support. Provide details of your subscripton ID, workspace name, and a business justification. The QCI support team will evaluate your request. https://aka.ms/AQ/QCI/CustomerSupport"
        },
        {
            "id": "quota_provider_type_1qloud",
            "visibility": "quota_subtype == provider-quota && quota_provider_name != MS-Quantum && quota_provider_name == 1Qloud",
            "order": 13,
            "controlType": "textBlock",
            "displayLabel":"To request a quota/limit increase for your 1Qloud Optimization Platform offer offer, reach out to 1QBit support. Provide details of your subscripton ID, workspace name, and a business justification. The 1QBit support team will evaluate your request. https://aka.ms/AQ/1QBit/CustomerSupport"
        },
        {
            "id": "quota_provider_new_limit",
            "visibility": "quota_subtype == provider-quota && quota_provider_workspace != null && quota_provider_workspace != dont_know_answer && quota_provider_name == MS-Quantum",
            "order": 14,
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
            "order": 15,
            "controlType": "multilinetextbox",
            "displayLabel": "Describe the business requirement",
            "watermarkText": "Provide business justification for your request",
            "required": false
        },
        {
            "id": "quota_provider_description_fallback",
            "visibility": "quota_provider_workspace == dont_know_answer || quota_provider_name == dont_know_answer",
            "order": 16,
            "controlType": "multilinetextbox",
            "displayLabel": "Describe your quota request",
            "useAsAdditionalDetails": true,
            "watermarkText": "Provide additional information about your issue, including details such as workspace name, region, type of limit, current value and new value requested as applicable.",
            "required": true
        }
    ]
}
---
