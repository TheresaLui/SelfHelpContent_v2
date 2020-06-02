<properties
	articleId="problemscopingques-issue-while-investigating-or-configuring-availability-tests"
	pageTitle="Issue while investigating or configuring Availability tests"
	description="Issue while investigating or configuring Availability tests"
	authors="neilghuman"
	ms.author="neghuman"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32729575, 32729576, 32729577, 32729582, 32729588"
	productPesIds="15693"
	cloudEnvironments="public,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureMonitoring_ApplicationInsights"
/>
# Issue while investigating or configuring Availability tests
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Issue while investigating or configuring Availability tests",
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
            "id": "classic_alert_id",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Please select the affected Availability Tests resource.",
            "watermarkText": "Choose an option",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionid}/resourcegroups/{resourcegroup}/providers/microsoft.insights/components/{resourcename}/webtests?noLargeObjects=true&skipConfig=true&api-version=2015-05-01",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$"
            },
            "dropdownOptions": [
                {
                    "value": "Unable to get the list of availability tests for this resource",
                    "text": "Unable to get the list of availability tests for this resource"
                }
            ],
            "required": false
        },
        {
            "id": "notification_type",
            "order": 3,
            "controlType": "multiselectdropdown",
            "displayLabel": "Where is the monitored application running?",
            "watermarkText": "Choose one or more",
            "dropdownOptions": [
                {
                    "value": "Azure VM",
                    "text": "Azure VM"
                },
                {
                    "value": "On-Premises VM",
                    "text": "On-Premises VM"
                },
                {
                    "value": "Azure Web App or App Service",
                    "text": "Azure Web App or App Service"
                },
                {
                    "value": "Azure Cloud Service",
                    "text": "Azure Cloud Service"
                },
                {
                    "value": "Azure Function",
                    "text": "Azure Function"
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
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Describe the problem you are noticing",
            "watermarkText": "Describe the problem you are noticing",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": []
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