<properties
	articleId="problemscopingques-enabling-data-collection-on-a-specific-platform-using-codeless-attach"
	pageTitle="Enabling data collection on a specific platform using codeless attach"
	description="Enabling data collection on a specific platform using codeless attach"
	authors="neilghuman"
	ms.author="neghuman"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32729587, 32729618, 32729619, 32729620, 32729621, 32729622, 32729623, 32729624, 32729615, 32729616,32729617"
	productPesIds="15693"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	schemaVersion="1"
	ownershipId="AzureMonitoring_ApplicationInsights"
/>
# Enabling data collection on a specific platform using codeless attach
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Enabling data collection on a specific platform using codeless attach",
    "fileAttachmentHint": "Please upload a screenshot(s) of the entire browser window displaying the symptom.  Kindly include an image of clock, and any other relevant information which may help the support engineer troubleshoot your issue.",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
        {
            "id": "notification_type",
            "order": 3,
            "controlType": "multiselectdropdown",
            "displayLabel": "What is the language of the monitored application experiencing the issue?",
            "watermarkText": "Choose one or more",
            "dropdownOptions": [
                {
                    "value": ".Net language",
                    "text": ".Net language"
                },
                {
                    "value": "Java",
                    "text": "Java"
                },
                {
                    "value": "Node.js",
                    "text": "Node.js"
                },
                {
                    "value": "Javascript",
                    "text": "Javascript"
                },
                {
                    "value": "Other",
                    "text": "Other"
                },
                {
                    "value": "dont_know_answer",
                    "text": "I don't know"
                }
            ],
            "required": true
        },
            {
            "id": "notification_type_other",
            "order": 4,
            "visibility": "notification_type == Other",
            "controlType": "textbox",
            "displayLabel": "What is the language of the monitored application experiencing the issue?",
            "watermarkText": "What is the language of the monitored application experiencing the issue?",
            "required": false
            },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Describe the problem you are seeing",
            "watermarkText": "Please include expected versus observed behavior, exact errors, etc",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Provide expected versus observed behavior"
                },
                {
                    "text": "Provide the exact errors"
                },
                {
                    "text": "Upload screenshots below as file attachments"
                }
            ]
        },
        {
            "id": "additional_information",
            "order": 9,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional information about the issue.",
            "watermarkText": "Provide any additional information about the issue.",
            "required": false,
            "useAsAdditionalDetails": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---