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
    "title": "No data in Application Insights",
    "fileAttachmentHint": "",
    "formElements": [{ 
            "id": "problem_start_time",
            "order": 1, 
            "controlType": "datetimepicker", 
            "displayLabel": "When did the problem start?", 
            "required": true 
        }, {
            "id": "problem_description",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        },{
			"id": "python_version",
			"order": 3,
			"controlType": "textbox",
			"displayLabel": "What version of Python are you using?",
			"required": false
		},{
			"id": "dependencies_version",
			"order": 4,
			"controlType": "multilinetextbox",
			"displayLabel": "List the version numbers of relevant installed dependencies.",
			"required": false
		},{
			"id": "instrumentation_code",
			"order": 5,
			"controlType": "multilinetextbox",
			"displayLabel": "Paste a code snippet of how you instrumented with OpenCensus.",
			"required": false
		}
	]
}
---
