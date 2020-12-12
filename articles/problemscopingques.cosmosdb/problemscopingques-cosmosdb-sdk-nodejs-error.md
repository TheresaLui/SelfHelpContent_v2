<properties
	pageTitle="CosmosDB Nodejs or Javascript SDK Exceptions"
	description="CosmosDB Nodejs or Javascript SDK Exceptions"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32783717"
	productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="5db08b83-4573-4f4b-b530-4d6558c562f4"
	ownershipId="AzureData_AzureCosmosDB"
/>
# CosmosDB Nodejs or Javascript SDK Exception Issues
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "CosmosDB Nodejs or Javascript SDK Exception Issues",
    "fileAttachmentHint": "Please attach at least 20 stack traces with the exception message in a single flat text file.",
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
            "id": "sdk_version",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "What is your SDK Version?",
			"infoBalloonText": "Version example (1.x.x, 2.x.x, 3.x.x)",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide repro steps or sample code for your issue.",
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