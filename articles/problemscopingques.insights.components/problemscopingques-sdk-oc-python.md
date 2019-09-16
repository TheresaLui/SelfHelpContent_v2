<properties
	articleId="problemscopingques-sdk-oc-python"
	pageTitle="OpenCensus Python SDK"
	description="OpenCensus Python SDK"
	authors="lechen"
	ms.author="lechen"
	selfHelpType="problemScopingQuestions"
	supportTopicIds=""
	productPesIds="15693"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# OpenCensus Python SDK
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "OpenCensus Python SDK",
    "fileAttachmentHint": "",
    "formElements": [{
			"id": "python_version",
			"order": 1,
			"controlType": "textbox",
			"displayLabel": "What version of Python are you using?",
			"required": false
		},{
			"id": "dependencies_version",
			"order": 2,
			"controlType": "multilinetextbox",
			"displayLabel": "List the version numbers of relevant installed dependencies.",
			"required": false
		},{
			"id": "instrumentation_code",
			"order": 3,
			"controlType": "multilinetextbox",
			"displayLabel": "Paste a code snippet of how you instrumented with OpenCensus.",
			"required": false
		},{
            "id": "problem_start_time",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide these details",
            "required": true,
            "watermarkText": "Please provide: a detailed scenario of the error condition, troubleshooting done so far, log files, timestamp, screenshots and any other relevant information.",
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Expected behavior, actual behavior"
                },
                {
                    "text": "Troubleshooting done so far"
                },
                {
                    "text": "Log Files"
                },
                {
                    "text": "Timestamps"
                },
                {
                    "text": "Screenshots"
                }
            ]
        }
	]
}
---
