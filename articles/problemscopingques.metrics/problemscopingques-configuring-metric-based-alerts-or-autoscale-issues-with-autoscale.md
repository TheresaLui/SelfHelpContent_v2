<properties
	articleId="problemscopingques-configuring-metric-based-alerts-or-autoscale-issues-with-autoscale"
	pageTitle="Configuring metric-based alerts or autoscale - Issues with autoscale"
	description="Configuring metric-based alerts or autoscale - Issues with autoscale"
    authors="neilghuman"
	ms.author="neghuman"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32684754"
	productPesIds="16250"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	schemaVersion="1"
	ownershipId="AzureMonitoring_AzureMetrics"
/>

# Configuring metric-based alerts or autoscale - Issues with autoscale"
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Configuring metric-based alerts or autoscale - Issues with autoscale",
    "fileAttachmentHint": "Please upload screenshots of all relevant details from the Azure portal.  Include any additional information which may help the support engineer troubleshoot your issue.",
    "formElements": [
                {
            "id": "alert_group_id",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Select the impacted autoscale setting.",
            "watermarkText": "Select the impacted autoscale setting",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionId}/providers/microsoft.insights/autoscalesettings?api-version=2015-04-01",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "Unable to get the list of autoscale settings",
                    "text": "Unable to get the list of autoscale settings"
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
            "displayLabel": "Provide details of at least one instance of the problem being experienced.",
            "watermarkText": "Provide details of at least one instance of the problem being experienced.",
            "required": true,
            "useAsAdditionalDetails": false,
            "hints": [
                {
                    "text": "Metric names"
                },
                {
                    "text": "Provide the timestamp and time zone"
                },
                {
                    "text": "If applicable, screenshot of the issue"
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