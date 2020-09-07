<properties
	pageTitle="CosmosDB SDK Other Issues"
	description="CosmosDB SDK Other Issues"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32741535,32688838"
	productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="593dd156-70b4-4197-9751-dd032af7a4cf"
	ownershipId="AzureData_AzureCosmosDB"
/>
# CosmosDB SDK Other Issues
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "CosmosDB SDK Other Issues",
    "fileAttachmentHint": "Attach (zip) file of sample code",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
		{
            "id": "environment_information",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Environment Information",
			"infoBalloonText": "Environment info (Azfunctions/App Service/VM, Other, Spark, Spring, Other Cloud)",
            "required": false
        },
		{
            "id": "region_information",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Region Information",
			"infoBalloonText": "Read/Write regions where the issue is experienced",
            "required": false
        },
		{
            "id": "sdk_type",
            "order": 4,
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
                    "value": "Spark",
                    "text": "Spark"
                }
            ],
            "required": false
        },
        {
            "id": "sdk_version",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "What is your SDK Version?",
			"infoBalloonText": "Version example (1.x.x, 2.x.x, 3.x.x)",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide repro steps and sample code for your issue.",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "To expedite your issue resolution it may help to provide steps to reproduce the issue and/or sample code attached as a file or link to git hub"
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---