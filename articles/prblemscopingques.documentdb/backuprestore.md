<properties
	pageTitle="CosmosDb Backup and Restore Info"
	description="CosmosDb Backup and Restore Info"
	authors="bharathsreenivas"
	selfHelpType="problemScopingQuestions" 
        supportTopicIds="32597495"
	productPesIds="15585"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# CosmosDb Backup and restore Info
---
{
	"resourceRequired": true,
	"title": "CosmosDb Backup and Restore Info",
	"fileAttachmentHint": "",
	"formElements": [
				{
			"id": "learn_more_text",
			"order": 1,
			"controlType": "infoblock",
			"content": "Cosmos DB has offers transparent regional failovers with multi-homing APIs. In case you are testing the backup/restore process for disaster recovery scenarios, you can use the <a href='https://docs.microsoft.com/azure/cosmos-db/regional-failover'>manual failover</a> capabilities of Cosmos DB"
		},
		 {
			"id": "problem_start_date",
			"order": 2,
			"controlType": "datetimepicker",
			"displayLabel": "What time did the problem begin?",
			"required": true
		  },
		  {
			"id": "database_name",
			"order": 3,
			"controlType": "textbox",
			"displayLabel": "Affected databases (separate with commas)",
			"required": true,
			"hints": [{
					"text": "Affected databases (separate with commas)"
				}]
		},
		{
			"id": "collection_name",
			"order": 4,
			"controlType": "textbox",
			"displayLabel": "Affected collections (separate with commas)",
			"required": true,
			"hints": [{
					"text": "Affected collections (separate with commas)"
				}]
		},
		{
			"id": "data_type",
			"order": 5,
			"controlType": "dropdown",
			"displayLabel": "What is the type of data to be restored?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "Production",
					"text": "Production"
				},{
					"value": "UAT",
					"text": "UAT"
				},{
					"value": "Test",
					"text": "Test"
				},{
					"value": "Demo",
					"text": "Demo"
				},{
					"value": "Other (describe below in the description)",
					"text": "Other (mention below in the description)"
				}
			],
			"required": false
		},
		{
			"id": "restore_objective",
			"order": 6,
			"controlType": "dropdown",
			"displayLabel": "What purpose of the restore?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": "To test disaster recovery",
					"text": "To test disaster recovery"
				},{
					"value": "To test restore process",
					"text": "To test restore process"
				},{
					"value": "To create a new environment (dev/test/staging/other)",
					"text": "To create a new environment (dev/test/staging/other)"
				},{
					"value": "To recover from accidental deletion of Cosmos DB Account",
					"text": "To recover from accidental deletion of Cosmos DB Account"
				},{
					"value": "To recover from accidental deletion of Cosmos DB Database",
					"text": "To recover from accidental deletion of Cosmos DB Database"
				},{
					"value": "To recover from accidental deletion of Cosmos DB Collection/Container",
					"text": "To recover from accidental deletion of Cosmos DB Collection/Container"
				},{
					"value": "To recover from accidental deletion or updation of data in a Cosmos DB Collection/Container",
					"text": "To recover from accidental deletion or updation of data in a Cosmos DB Collection/Container"
				},{
					"value": "Other (describe below in the description)",
					"text": "Other (mention below in the description)"
				}
			],
			"required": true
		},
		{
			"id": "issue-details",
			"order": 7,
			"controlType": "multilinetextbox",
			"displayLabel": "Please provide additional details about the restore request. ",
			"required": false,
			"useAsAdditionalDetails": true
		}
                ]
                }
---
