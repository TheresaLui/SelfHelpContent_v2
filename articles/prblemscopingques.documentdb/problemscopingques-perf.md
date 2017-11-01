<properties
	pageTitle="CosmosDb Performance Issue"
	description="CosmosDb Performance Issue"
	authors="bharathsreenivas"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32574375,32574400,32574404,32574304,32574412,32574419,32574426"
	productPesIds="15585"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# CosmosDb performance Issue
---
{
	"resourceRequired": true,
	"title": "CosmosDb Performance Issue",
	"fileAttachmentHint": "",
	"formElements": [
      {
			"id": "problem_start_date",
			"order": 1,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": false
		  },
		  {
			"id": "performance_issue_details",
			"order": 2,
			"controlType": "multilinetextbox",
			"displayLabel": "Please provide details about the issue that you were facing.",
			"required": false,
			"useAsAdditionalDetails": true,
			"hints": [{
					"text": "Activity Id of the request."
				}, {
					"text": "Name of the collection"
				}, {
					"text": "Name of the database."
				}, {
					"text": "Details on the exact issue."
				}
			]
		},
		{
			"id": "sdk_type",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "What is the client SDK used?",
			"watermarkText": "Choose an option",
			"dropdownOptions": [{
					"value": ".NET",
					"text": ".NET"
				},{
					"value": "Java",
					"text": "Java"
				},{
					"value": "Node.js",
					"text": "Node.js"
				},{
					"value": "Python",
					"text": "Python"
				},{
					"value": "Other (describe below)",
					"text": "Other (mention below in the description)"
				}
			],
			"required": false
		},
    		{
			"id": "sdk_version",
			"order": 4,
			"controlType": "textbox",
			"displayLabel": "SDK Version",
			"required": false,
			"useAsAdditionalDetails": true,
			"hints": [{
					"text": "SDK Version"
				}]
		},
		{
			"id": "learn_more_text",
			"order": 5,
			"controlType": "infoblock",
			"content": "<a href='https://docs.microsoft.com/en-us/azure/cosmos-db/performance-tips'>Learn more</a> about how to tune your the performance of your CosmosDb account"
		}
	]
}
---
