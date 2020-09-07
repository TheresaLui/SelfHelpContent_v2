<properties
	articleId="writing-queries-or-visualizing-results-in-log-analytics"
	pageTitle="Writing queries or visualizing results in Log Analytics"
	description="Writing queries or visualizing results in Log Analytics"
	authors="neilghuman"
	ms.author="neghuman"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32729595, 32729602"
	productPesIds="15693"
	cloudEnvironments="public,fairfax,mooncake, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureMonitoring_ApplicationInsights"
/>
# Writing queries or visualizing results in Log Analytics
---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Writing queries or visualizing results in Log Analytics",
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
            "displayLabel": "Describe the problem you are seeing",
            "watermarkText": "Please include expected versus observed behavior, exact errors, the Request id, etc",
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
                    "text": "Provide the Request id"
                },
                {
                    "text": "Upload screenshots below as additional file attachments"
                }
            ]
        },
        {
            "id": "query",
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "Please paste in the query you are trying to use.",
            "watermarkText": "Please paste in the query you are trying to use.",
            "required": false,
            "useAsAdditionalDetails": false
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