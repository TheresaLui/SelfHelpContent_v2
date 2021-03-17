<properties
	articleId="problemscopingques-an-alert-was-not-fired-when-it-should"
	pageTitle="An alert was not fired when it should"
	description="An alert was not fired when it should"
	authors="neilghuman"
	ms.author="neghuman"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32739794, 32739768, 32739784, 32739813, 32739789, 32739809"
	productPesIds="15454"
	cloudEnvironments="public,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureMonitoring_ActionGroup"
/>
# An alert was not fired when it should
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "An alert was not fired when it should",
    "fileAttachmentHint": "Please upload screenshots of all relevant details from the Azure portal.  Include any details outlining why the alert should have fired and additional information which may help the support engineer troubleshoot your issue.",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start happening?",
            "required": false
        },
                {
            "id": "problem_frequency",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "How frequently does the problem occur?",
            "watermarkText": "How frequently does the problem occur?",
            "required": true,
            "dropdownOptions": [
                {
                    "value": "Once",
                    "text": "Issue occurred once only"
                },
                {
                    "value": "Multiple",
                    "text": "Issue occurred more than once but not always"
                },
                {
                    "value": "Ongoing",
                    "text": "Issue occurs for every alert instance"
                },
                {
                    "value": "dont_know_answer",
                    "text": "I don't know"
                }
            ]
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide details of at least one instance when the alert should have fired but didn't.",
            "watermarkText": "Provide details of at least one instance when the alert should have fired but didn't.",
            "required": true,
            "useAsAdditionalDetails": false,
            "hints": [
                {
                    "text": "Provide the timestamp and time zone"
                },
                {
                    "text": "Explanation of why the alert should have fired"
                },
                {
                    "text": "Screenshot of any details outlining why the alert should have fired"
                }
            ]
        },
        {
            "id": "additional_information",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional information about the issue.",
            "watermarkText": "Provide any additional information about the issue.",
            "required": false,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---