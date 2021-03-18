<properties
	pageTitle="Cosmos DB Python SDK Performance Issues"
	description="Cosmos DB Python SDK Performance Issues"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32783726"
	productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="33a92887-a33b-42bd-b55c-98baf79d0e4a"
	ownershipId="AzureData_AzureCosmosDB"
/>
# Cosmos DB Python SDK Performance Issues
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Cosmos DB Python SDK Performance Issues",
    "fileAttachmentHint": "Please attach a memory dump, netstat information, and CPU logs (zip file)",
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
            "id": "environment_information",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Environment Information",
			"infoBalloonText": "Environment info (Azfunctions/App Service/VM, Other, Spark, Spring, Other Cloud)",
            "required": false
        },
		{
            "id": "region_information",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Region Information",
			"infoBalloonText": "Read/Write regions where the issue is experienced",
            "required": false
        },
        {
            "id": "sdk_version",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "What is your SDK Version?",
			"infoBalloonText": "Version example (1.x.x, 2.x.x, 3.x.x)",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional details about the issue that you are facing",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "More information on the exact issue."
                },
                {
                    "text": "Please provide repro steps."
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---