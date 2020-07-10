<properties
	articleId="problemscopingques-issue-with-activity-log-alerts"
	pageTitle="Issues with Activity Log Alerts"
	description="Issues with Activity Log Alerts"
	authors="neilghuman"
	ms.author="neghuman"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32684686"
	productPesIds="16251"
	cloudEnvironments="public,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureMonitoring_ActionGroup"
/>
# Issues with Activity Log Alerts
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Issues with Activity Log Alerts",
    "fileAttachmentHint": "Please upload screenshots of all relevant details from the Azure portal.  Include any additional information which may help the support engineer troubleshoot your issue.",
    "formElements": [
                {
            "id": "action_group_id",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Select the impacted Action Rule resource.",
            "watermarkText": "Choose an action rule",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionid}/providers/microsoft.alertsmanagement/actionRules?api-version=2019-05-05-preview",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "Unable to get the list of Action rules",
                    "text": "Unable to get the list of Action rules"
                }
            },
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start happening?",
            "required": false
        },
        {
            "id": "problem_frequency",
            "order": 3,
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
            "order": 4,
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
            "order": 5,
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