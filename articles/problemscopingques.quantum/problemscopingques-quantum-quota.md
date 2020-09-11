<properties
    pageTitle="Quota Scoping questions for Azure Quantum"
    description="Quota Scoping questions for Azure Quantum"
    authors="dasto"
    ms.author="dasto"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="NEED QUOTA SUPPORT TOPIC"
    productPesIds="17040"
    cloudEnvironments="Public"
    schemaVersion="1"
    articleId="problemscopingques-quantum-quota"
    ownershipId="AzureCompute_AzureQuantum"
/>
# Azure Quantum Quota Questions
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "AzureQuantum-Quota",
    "fileAttachmentHint": "",
    "quotaRequestVersion": "0.0",
    "formElements": [
        {
            "id": "quota_subtype",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Choose the provider that this quota request relates to...",
            "watermarkText": null,
            "required": "true",
            "filter": false,
            "includeInQuotaSummary": true,
            "dropdownOptions": [
                {
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
                    "text": "Other",
                    "value": "dont_know_answer"
                }
            ]
        },
        {
			"id": "quota_workspacename",
			"visibility": "quota_subtype != null",
			"order": 2,
			"controlType": "dropdown",
			"displayLabel": "Choose the Azure Quantum workspace that you are requesting the quota for...",
			"required": false,
			"dynamicDropdownOptions": {
				"dependsOn": "quotaSubType",
                "uri": "/subscriptions/{subscriptionId}/providers/Microsoft.Quantum/Workspaces?api-version=2019-11-04-preview",
                "jTokenPath": "value",
                "textProperty": "name,location",
                "textTemplate": "Name:{name}, Region:{location}",
                "valueProperty": "id",
				"valuePropertyRegex": "^*$",
				"defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            }
        },
        {
            "id": "capacity_requested",
            "visibility": "quota_subtype != null && quota_workspacename != null && quota_workspacename != 'dont_know_answer'",
            "order": 3,
            "controlType": "numerictextbox",
            "isNewQuotaLimit": true,
            "includeInQmsPayload": true,
            "displayLabel": "Capacity requested (in job execution minutes)",
            "required": true,
            "validations": [
                            {
                             "type": "greaterthan",
                             "value": 0
                            }
                           ]
        },
        {
            "id": "business_justification",
            "visibility": "quota_subtype != null",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Describe the business requirement",
            "watermarkText": "Provide business justification for your request",
            "required": false
        },
        {
            "id": "problem_description",
            "visibility": "quota_subtype != null",
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