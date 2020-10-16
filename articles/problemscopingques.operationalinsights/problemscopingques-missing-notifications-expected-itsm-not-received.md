<properties
	articleId="problemscopingques-missing-notifications-expected-itsm-not-received-la"
	pageTitle="Expected itsm not received"
	description="Expected itsm not received"
	authors="neilghuman"
	ms.author="neghuman"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32745404"
	productPesIds="15725"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	schemaVersion="1"
	ownershipId="AzureMonitoring_LogAnalytics"
/>
# Not receiving notifications
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Not receiving notifications",
    "fileAttachmentHint": "Please upload screenshots of all relevant details from the Azure portal.  Kindly include Alert id, Fired time, and any other relevant information which may help the support engineer troubleshoot your issue.",
    "formElements": [
        {
            "id": "action_group_id",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Select the affected Action Group resource.",
            "watermarkText": "Choose an action group",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionid}/providers/microsoft.insights/actionGroups?api-version=2017-04-01",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "Unable to get the list of Action groups",
                    "text": "Unable to get the list of Action groups"
                }
            },
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start happening?",
            "required": true
        },
        {
            "id": "problem_frequency",
            "order": 4,
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