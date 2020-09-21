<properties
	pageTitle="Slow Performance SQL MIAA Instance"
	description="Slow Performance SQL MIAA Instance"
	ms.author="amigan,jopilov,prmadhes"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32743949"
	productPesIds="17125"
	cloudEnvironments="Public"
	schemaVersion="1"
	articleId="1A9C95E8-97DF-40A8-B0BE-AB23C5BA40B4"
	ownershipId="AzureData_Managed_Instance_Azure_Arc"
/>
# Slow Performance SQL MIAA Instance
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": false,
  "resourceRequired": false,
	"title": "SQL Server - Azure Arc",
	"fileAttachmentHint": "",
	"formElements": [
		{
			"id": "problem_start_time",
			"order": 1,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
		}, {
			"id": "slow_component",
			"order": 2,
			"controlType": "dropdown",
			"displayLabel": "What component is slow in SQL Server?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "query(s)",
					"text": "query(s)"
				}, {
					"value": "backup",
					"text": "backup"
				}, {
					"value": "SQL replication",
					"text": "SQL replication"
				}, {
					"value": "overall server",
					"text": "overall server"
				}, {
					"value": "bulk data processing",
					"text": "bulk data processing"
				}, {
					"value": "DBCC CHECKDB",
					"text": "DBCC CHECKDB"
				}, {
					"value": "stats or index operations",
					"text": "stats or index operations"
				}, {
					"value": "dont_know_answer",
					"text": "I’m not sure/don’t know"
				}
			],
			"required": true
		}, {
			"id": "baseline_sql",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "What baseline are you using to establish things are slow?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "it previous ran faster on this MIAA instance",
					"text": "it previous ran faster on this MIAA instance"
				}, {
					"value": "it is faster on another environment that runs this workload",
					"text": "it is faster on another environment that runs this workload"
				}, {
					"value": "I am not sure/don't have a baseline",
					"text": "I am not sure/don't have a baseline"
				}, {
					"value": "dont_know_answer",
					"text": "I’m not sure/don’t know"
				}
			],
			"required": true
		}, {
			"id": "bottlenecks_types",
			"order": 4,
			"controlType": "multilinetextbox",
			"displayLabel": "What wait types bottlenecks did you observe during query execution, if any?",
			"required": false
		}, {
			"id": "troubleshooting_attempted",
			"order": 5,
			"controlType": "multilinetextbox",
			"displayLabel": "What troubleshooting steps have you attempted?",
			"required": false
		}, {
			"id": "problem_description",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Issue Description",
			"watermarkText": "Provide additional information about your issue.",
            "useAsAdditionalDetails": true,
            "required": true
		}
	]
}
---
