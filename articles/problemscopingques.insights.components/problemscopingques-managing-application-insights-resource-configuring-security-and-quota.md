<properties
	articleId="problemscopingques-managing-application-insights-resource-configuring-security-and-quota"
	pageTitle="Managing Application Insights resource, Configuring Security, and Quota"
	description="Managing Application Insights resource, Configuring Security, and Quota"
	authors="neilghuman"
	ms.author="neghuman"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32729593,32729600,32729596,32729597"
	productPesIds="15693"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	schemaVersion="1"
	ownershipId="AzureMonitoring_ApplicationInsights"
/>
# Managing Application Insights resource, Configuring Security, and Quota
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Managing Application Insights resource, Configuring Security, and Quota",
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
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Describe the problem you are seeing (please include expected versus observed behavior, exact errors, etc)",
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
            "id": "notification_type_other",
            "order": 4,
            "visibility": "notification_type == Other",
            "controlType": "textbox",
            "displayLabel": "If you need to recover, rename, or move an Application Insights Component, what is the specific name of the component and the resource group where it resides?",
            "watermarkText": "If you need to recover, rename, or move an Application Insights Component, what is the specific name of the component and the resource group where it resides?",
            "required": false
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