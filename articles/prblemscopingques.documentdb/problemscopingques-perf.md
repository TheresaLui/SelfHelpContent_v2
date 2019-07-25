<properties
	pageTitle="CosmosDB Performance Issue"
	description="CosmosDB Performance Issue"
	authors="rnagpal"
	ms.author="rnagpal"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32636818"
	productPesIds="15585"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="b0c21976-936c-466a-801c-0eca87e1ab5a"
/>
# CosmosDB performance Issue
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "CosmosDB Performance Issue",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "learn_more_text",
            "order": 1,
            "controlType": "infoblock",
            "content": "Use the <a href='https://docs.microsoft.com/azure/cosmos-db/performance-tips'>Performance Tuning Guide</a> to learn more about how you can improve the performance of your database"
        },
        {
            "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "database_name",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Database name",
            "required": false
        },
        {
            "id": "collection_name",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Collection name",
            "required": false
        },
        {
            "id": "sdk_type",
            "order": 5,
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
                    "value": "Node.js",
                    "text": "Node.js"
                },
                {
                    "value": "Python",
                    "text": "Python"
                },
                {
                    "value": "Other (describe below)",
                    "text": "Other (mention below in the description)"
                }
            ],
            "required": false
        },
        {
            "id": "sdk_version",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "SDK Version",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional details about the issue that you were facing.",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Details on the exact issue."
                },
                {
                    "text": "Activity Id of the request (if available)."
                },
                {
                    "text": "Read/Write regions where the issue is being experienced."
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---
