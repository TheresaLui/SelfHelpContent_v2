<properties
	pageTitle="Advisory questions - queue"
	description="Advisory questions"
	authors="Sijia"
  ms.author="siz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32681656"
	productPesIds="16461"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	articleId="81697623-be85-446a-b6b0-c02c07f48129"
	ownershipId="StorageMediaEdge_StorageQueues"
/>

# Monitoring - Advisory questions
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Monitoring advisory questions",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Need advisory on Monitoring related questions?",
        "description": "Our Monitor Advisory troubleshooter can help you troubleshoot and solve your problem.",
        "insightNotAvailableText": "Our troubleshooter did not detect any issues with your resource. Please ensure the information provided is accurate and in the approved format. Also, see our manual troubleshooting steps below to troubleshoot your problem."
	},
    "formElements": [
        {
            "id": "queue_names",
            "order": 1,
            "controlType": "multiselectdropdown",
            "displayLabel": "Queue Names",
            "watermarkText": "Select from your queues",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionId}/resourceGroups/{resourcegroup}/providers/Microsoft.Storage/storageAccounts/{resourcename}/queueServices/default/queues?api-version=2019-06-01",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "name",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Not applicable/No queues available"
                }
            }
        },
        {
            "id": "monitor_advisory",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Monitor advisory question",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "cost_question",
                    "text": "Cost related question"
                },
                {
                    "value": "log_retention",
                    "text": "Log retention question"
                },
                {
                    "value": "audit_action",
                    "text": "Action audit question"
                },
		            {
                    "value": "dont_know_answer",
                    "text": "Don't know or not listed above"
                }
            ],
            "required": true,
	    "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate start time of the most recent occurrence",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional details",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
