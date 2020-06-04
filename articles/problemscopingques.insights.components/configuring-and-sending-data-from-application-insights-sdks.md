<properties
	articleId="configuring-and-sending-data-from-application-insights-sdks"
	pageTitle="Configuring and sending data from Application Insights SDKs"
	description="Configuring and sending data from Application Insights SDKs"
	authors="neilghuman"
	ms.author="neghuman"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32729599, 32729603, 32729604, 32729605, 32729606, 32729609, 32729612"
	productPesIds="15693"
	cloudEnvironments="public,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureMonitoring_ApplicationInsights"
/>
# Configuring and sending data from Application Insights SDKs
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Configuring and sending data from Application Insights SDKs",
    "fileAttachmentHint": "Please upload a screenshot(s) of the entire browser window displaying the symptom.  Kindly include an image of clock, and any other relevant information which may help the support engineer troubleshoot your issue.",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start occurring?",
            "required": true
        },
        {
            "id": "notification_type",
            "order": 3,
            "controlType": "multiselectdropdown",
            "displayLabel": "Where is the monitored application deployed?",
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
            "id": "notification_type_other",
            "order": 5,
            "visibility": "notification_type == Other",
            "controlType": "textbox",
            "displayLabel": "Please describe how the application is deployed:",
            "watermarkText": "Kubernetes, Cloud Provider XYZ",
            "required": false
        },
            {
            "id": "site_app",
            "order": 7,
            "visibility": "depend != null",
            "controlType": "textbox",
            "displayLabel": "What is the name of the site/app that is related to this issue?",
            "watermarkText": "What is the name of the site/app that is related to this issue?",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 9,
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
            "id": "availability_test_reason",
            "order": 11,
            "controlType": "dropdown",
            "displayLabel": "Do you believe there is a problem with the data Application Insights is presenting or are you looking for guidance on resolving an error? ",
            "dropdownOptions": [
                {
                    "value": "Application Insights data correct but help needed fixing an error",
                    "text": "Application Insights data correct but help needed fixing an error"
                },
                {
                    "value": "Application Insights data looks incorrect",
                    "text": "Application Insights data looks incorrect"
                },
                {
                    "value": "dont_know_answer",
                    "text": "I don't know"
                }
            ],
            "required": true
        },
        {
            "id": "additional_information",
            "order": 13,
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