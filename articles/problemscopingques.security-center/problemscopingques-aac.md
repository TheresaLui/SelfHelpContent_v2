<properties
	pageTitle="Azure Defender - Adaptive Application Control (AAC)"
	description="Azure Defenderr - Adaptive Application Control (AAC)"
	authors="orbarak-ms"
	ms.author="orbarak"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32693228"
    productPesIds="15947"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    articleId="scoping_asc_aac"
	schemaVersion="1"
	ownershipId="Azure_Security_Security_Center"
/>
# Adaptive Application Control (AAC)
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "32693228",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "acc_issuetype",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Select the option that best matches the issue you're experiencing",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "enable_vm",
                    "text": "Enable application controls on virtual machines"
                },
                {
                    "value": "Group configuration",
                    "text": "Enable application controls on a group "
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other issues with adaptive application control"
                }
            ],
            "required": true
        },
        {
            "id": "problem_description",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---
