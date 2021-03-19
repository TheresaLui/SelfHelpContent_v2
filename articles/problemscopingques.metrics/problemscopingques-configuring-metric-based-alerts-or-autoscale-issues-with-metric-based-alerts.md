<properties
	articleId="problemscopingques-configuring-metric-based-alerts-or-autoscale-issues-with-metric-based-alerts"
	pageTitle="Configuring metric-based alerts or autoscale - Issues with metric-based alerts"
	description="Configuring metric-based alerts or autoscale - Issues with metric-based alerts"
    authors="neilghuman"
	ms.author="neghuman"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32684755"
	productPesIds="16250"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	schemaVersion="1"
	ownershipId="AzureMonitoring_AzureMetrics"
/>

# Configuring metric-based alerts or autoscale - Issues with metric-based alerts"
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Configuring metric-based alerts or autoscale - Issues with metric-based alerts",
    "fileAttachmentHint": "Please upload screenshots of all relevant details from the Azure portal.  Include any additional information which may help the support engineer troubleshoot your issue.",
    "formElements": [
                {
            "id": "alert_group_id",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Select the impacted metric rule.",
            "watermarkText": "Choose a metric rule",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionId}/providers/Microsoft.Insights/metricAlerts?api-version=2018-03-01",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "Unable to get the list of metric rules",
                    "text": "Unable to get the list of metric rules"
                }
            },
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start happening?",
            "required": false
        },
                {
            "id": "problem_frequency",
            "order": 5,
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
            "order": 7,
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
            "order": 9,
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