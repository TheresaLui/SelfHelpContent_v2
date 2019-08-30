<properties
	pageTitle="CosmosDB SDK Exception Issues"
	description="CosmosDB SDK Exception Issues"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="problemScopingQuestions" 
	supportTopicIds="32636796"
	productPesIds="15585"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="dbc187be-a04d-40ef-9012-be95a0993db7"
/>
# CosmosDB SDK Exception Issues
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "CosmosDB SDK Exception Issues",
    "fileAttachmentHint": "Please attach at least 20 stack traces wtih the exception message in a single flat text file.",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "previous_steps",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "What steps have you taken to resolve the issue?",
			"infoBallonText": "Provide steps and include URLs to documents, git hub, stack overflow, forms, etc. that you have already searched to help us improve",
			"required": false
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
            "displayLabel": "Percentage of requests seeing the exception",
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
            "id": "problem_description",
            "order": 9,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional details about the issue that you are facing",
            "required": false,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "More information on the exact issue."
                },
                {
                    "text": "Activity Id of the request (if available)."
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---