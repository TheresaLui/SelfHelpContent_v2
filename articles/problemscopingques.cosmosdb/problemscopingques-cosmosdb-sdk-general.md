<properties
	pageTitle="CosmosDB SDK General Questions"
	description="CosmosDB SDK General Questions"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32688840"
	productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	schemaVersion="1"
	articleId="3aab4fb2-c4f9-4828-a570-9a1f410a74e6"
	ownershipId="AzureData_AzureCosmosDB"
/>
# CosmosDB SDK General Questions
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "CosmosDB SDK General Questions",
    "fileAttachmentHint": "Attach any related screenshots or information",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
		{
            "id": "sdk_type",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Which SDK are you inquiring about?",
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
           "id": "question",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What is your question?",
			"infoBalloonText": "This form is for general Cosmos DB SDK questions. If you have a specific issue, please go back and select another SDK Issues problem subtype to expedite a resolution for your issue.",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Where did you already look?",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Provide URLs to documents, git hub, stack overflow, forms, etc. that you have already searched to help us improve"
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---