<properties
	pageTitle="CosmosDB SDK Other Issues"
	description="CosmosDB SDK Other Issues"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="problemScopingQuestions" 
	supportTopicIds="32636812"
	productPesIds="15585"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="26a8480b-f0c7-49a7-983e-f95c49822cb5"
/>
# CosmosDB SDK Other Issues
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "CosmosDB SDK Other Issues",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
		{
            "id": "problem_description",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide details about the issue that you are facing",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Details of the issue and frequency"
                }
            ]
        },
        {
            "id": "cpu_information",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "CPU Information",
            "required": false
        },
		{
            "id": "environment_information",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Environment Information",
			"infoBalloonText": "Environment info (Azfunctions/App Service/VM, Other, SPARK, Other Cloud)",
            "required": false
        },
		{
            "id": "region_information",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "Region Information",
			"infoBalloonText": "Read/Write regions where the issue is experienced",
            "required": false
        },
		{
            "id": request_pct",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "Percentage of requests observing the issue",
            "required": false
        },
		{
            "id": "sdk_type",
            "order": 7,
            "controlType": "dropdown",
            "displayLabel": "What is the client SDK used?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": ".NET",
                    "text": ".NET"
                },
                {
                    "value": "Java",
                    "text": "Java"
                },
                {
                    "value": "Java Script or Node.js",
                    "text": "Java Script or Node.js"
                },
                {
                    "value": "Python",
                    "text": "Python"
                },
                {
                    "value": "Spring",
                    "text": "Spring"
                },
                {
                    "value": "SPARK",
                    "text": "SPARK"
                }
            ],
            "required": false
        },
        {
            "id": "sdk_version",
            "order": 8,
            "controlType": "textbox",
            "displayLabel": "What is your SDK Version?",
			"infoBalloonText": "Version example (1xx, 2xx, 3xx)",
            "required": false
        },
        {
            "id": "problem_repro",
            "order": 9,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide repro steps and sample code for your issue",
			"infoBallonText": "To expedite your issue resolution it may help to provide steps to reproduce the issue and/or sample code",
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---