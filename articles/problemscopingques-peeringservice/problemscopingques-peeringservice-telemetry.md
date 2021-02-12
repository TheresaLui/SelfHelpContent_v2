<properties
	articleId="problemscopingques-peeringservice-telemetry"
	pageTitle="Scoping Questions for Peering Service Telemetry (Metrics, Prefix Events)"
	description="Scoping Questions for Peering Service Telemetry (Metrics, Prefix Events)"
	authors="brianlehr"
    ms.author="blehr"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32689971"
	productPesIds="16932"
	cloudEnvironments="public,mooncake,fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="Peering_PeeringService"
/>

# Telemetry Scoping Questions
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Peering Service Configuration",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "prefix_metric_issue",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Is there an issue with the Prefix Metrics (e.g. no latency results available, measurements look incorrect, etc)?  Please provide additional details.",
            "watermarkText": "Please provide details on the issue with Prefix Metrics",
            "required": false
        },
        {
            "id": "prefix_event_issue",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Is there an issue with the Prefix Metrics (e.g. no events showing, need help understanding event messages)?  Please provide additional details.",
            "watermarkText": "Please provide error message",
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---