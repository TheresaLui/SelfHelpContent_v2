<properties
	pageTitle="Recommendation Exemption"
	description="Recommendation Exemption"
	authors="genlin"
	ms.author="kawilson"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32693235"
    productPesIds="15947"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    articleId="b1b6273d-0021-4f2d-9112-36a830ea0107"
	schemaVersion="1"
	ownershipId="Azure_Security_Security_Center"
/>
# Recommendation Exemption in security center
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Recommendation Exemption in security center",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "resource_type",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Enter the name of recommendations that you want to exempt",
            "required": false
        },
        {
            "id": "scope_exempt",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Select the scope of the exemption",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "option_1",
                    "text": "Management Group"
                },
                {
                    "value": "option_2",
                    "text": "Subscriptions"
                },
                {
                    "value": "option_3",
                    "text": "Resources"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other"
                }
            ],
            "required": true
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---
