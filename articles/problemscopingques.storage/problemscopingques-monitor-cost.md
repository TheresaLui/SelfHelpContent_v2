<properties
	pageTitle="Advisory questions"
	description="Advisory questions"
	authors="Sijia"
        ms.author="siz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32681644,32681663,32681643,32681419,32681424,32681650,32681423,32681422,32681425"
	productPesIds="15629,16459,16460,16461,16462,16598"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest"
	schemaVersion="1"
	articleId="c449c5cc-78a3-4ef0-88a0-3c4622437a24"
/>

# Monitoring - Advisory questions
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Monitoring Help me understand metrics",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "monitor_advisory",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Monitor advisory question",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "cost_question",
                    "text": "Cost related question"
                },
                {
                    "value": "container_capacity",
                    "text": "Container capacity question"
                },
                {
                    "value": "log_retention",
                    "text": "Log retention question"
                },
                {
                    "value": "audit_action",
                    "text": "Action audit question"
                }
            ],
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate start time of the most recent occurrence",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional details",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
