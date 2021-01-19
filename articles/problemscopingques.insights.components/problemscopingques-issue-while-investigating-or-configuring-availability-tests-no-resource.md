<properties
	articleId="problemscopingques-issue-while-investigating-or-configuring-availability-tests-no-resource"
	pageTitle="Issue while investigating or configuring Availability tests"
	description="Issue while investigating or configuring Availability tests"
	authors="neilghuman"
	ms.author="neghuman"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32729575,32729576,32729577,32729582,32729588"
	productPesIds="15693"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	schemaVersion="1"
	ownershipId="AzureMonitoring_ApplicationInsights"
/>
# Issue while investigating or configuring Availability tests
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Issue while investigating or configuring Availability tests",
    "fileAttachmentHint": "Please upload a screenshot(s) of the entire browser window displaying the symptom.  Kindly include an image of clock, and any other relevant information which may help the support engineer troubleshoot your issue.",
    "diagnosticCard": {
        "title": "Availability Test Troubleshooter",
        "description": "Our Availability Test Troubleshooter can help you troubleshoot and solve your problem.",
        "insightNotAvailableText": "Our troubleshooter did not detect any issues with your resource. See our manual troubleshooting steps below to troubleshoot your problem."
    },
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true,
            "diagnosticInputRequiredClients": "Portal, ASC"
        },
        {
            "id": "notification_type",
            "order": 5,
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
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "Describe the problem you are noticing.",
            "watermarkText": "Describe the problem you are noticing.",
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