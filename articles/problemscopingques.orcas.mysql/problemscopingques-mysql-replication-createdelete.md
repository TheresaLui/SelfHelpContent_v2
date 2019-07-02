<properties
	pageTitle="Replication"
	description="Replication"
	authors="Hang-Zhang"
	ms.author="haz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32640050"
	productPesIds="16221"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="problemscopingques-mysql-replication-create_delete"
/>
# Replication - Create or delete read replicas
---
{
	"resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Replication Create delete read replicas",
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
            "id": "master_name",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "What is the server name and region of your master server?",
            "required": true
        },
        {
            "id": "replica_name",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What is the server name and region of your replica server?",
            "required": true
        },
		{
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Problem description",
            "watermarkText": "Provide your repro steps and other information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
	],
	"$schema": "SelfHelpContent"
}
---
