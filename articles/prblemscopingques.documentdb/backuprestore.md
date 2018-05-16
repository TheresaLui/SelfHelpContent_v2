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
# CosmosDb Backup and restoren Info
---
{
	"resourceRequired": true,
	"title": "CosmosDb Account and Collection Info",
	"fileAttachmentHint": "",
	"formElements": [
		 {
			"id": "problem_start_date",
			"order": 1,
			"controlType": "datetimepicker",
			"displayLabel": "In  did the problem begin?",
			"required": false
		  },
		  {
			"id": "database_name",
			"order": 2,
			"controlType": "textbox",
			"displayLabel": "Databases",
			"required": true,
			"hints": [{
					"text": "Affected databases (separate with commas)"
				}]
		},
		{
			"id": "collection_name",
			"order": 3,
			"controlType": "textbox",
			"displayLabel": "Collections",
			"required": true,
			"hints": [{
					"text": "Affected collections (separate with commas)"
				}]
		},
    {
			"id": "data_type",
			"order": 4,
			"controlType": "textbox",
			"displayLabel": "Type of data to be restored (Production/UAT/Test/Demo)",
			"required": true,
			"hints": [{
					"text": "Type of data to be restored (Production/UAT/Test/Demo)"
				}]
		},
		{
			"id": "issue-details",
			"order": 5,
			"controlType": "multilinetextbox",
			"displayLabel": "Please provide additional details about the restore request. In case you are testing for disaster recovery, you can use the [manual failover](https://docs.microsoft.com/azure/cosmos-db/regional-failover) capabilities of Cosmos DB",
			"required": false,
			"useAsAdditionalDetails": true,
			"hints": [
				{
					"text": "Is the restore request to test the restore process?"
				},{
					"text": "Is the restore request to recover from accidental deletion of database or collection?"
				},{
					"text": "Is the restore request to recover from accidental deletion/updation/insertion of data?"
				}
			]
		}
                ]
                }
---
