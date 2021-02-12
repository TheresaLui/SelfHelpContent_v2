<properties
	articleId="problemscopingques-problemscopingques-an-alert-fired-when-it-shouldnt-have"
	pageTitle="An alert fired when it shouldn't have"
	description="An alert fired when it shouldn't have"
	authors="neilghuman"
	ms.author="neghuman"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32739793, 32739766, 32739783, 32739812, 32739788, 32739808"
	productPesIds="15454"
	cloudEnvironments="public,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureMonitoring_ActionGroup"
/>
# An alert fired when it should not have
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "An alert fired when it should not have",
    "fileAttachmentHint": "Please upload screenshots of all relevant details from the Azure portal.  Include any additional information which may help the support engineer troubleshoot your issue.",
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
            "displayLabel": "Provide details of at least one Alert instance.",
            "watermarkText": "Provide details of at least one Alert instance.",
            "required": true,
            "useAsAdditionalDetails": false,
            "hints": [
                {
                    "text": "Provide the Alert id as seen in Azure portal"
                },
                {
                    "text": "Provide the timestamp and time zone (Fired time)"
                },
                {
                    "text": "Screenshot of the alert instance"
                },
                {
                    "text": "<a href='https://docs.microsoft.com/azure/azure-monitor/platform/alerts-managing-alert-instances#find-alert-instances'>Learn more about finding Alert instances</a>"
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