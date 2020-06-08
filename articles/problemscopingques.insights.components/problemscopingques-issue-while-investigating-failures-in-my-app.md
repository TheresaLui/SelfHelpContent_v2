<properties
	articleId="problemscopingques-issue-while-investigating-failures-in-my-app"
	pageTitle="Issue while investigating failures in my app"
	description="Issue while investigating failures in my app"
	authors="neilghuman"
	ms.author="neghuman"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32729570, 32729573, 32729578, 32729580, 32729583, 32729613, 32729625, 32729627, 32729628, 32729630, 32729632"
	productPesIds="15693"
	cloudEnvironments="public,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureMonitoring_ApplicationInsights"
/>
# Issue while investigating failures in my app
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Issue while investigating failures in my app",
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
            "id": "notification_type_other",
            "order": 4,
            "visibility": "notification_type == Other",
            "controlType": "textbox",
            "displayLabel": "Please describe how the monitored application is deployed:",
            "watermarkText": "Kubernetes, Cloud Provider XYZ",
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
            "id": "availability_test_reason",
            "order": 7,
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