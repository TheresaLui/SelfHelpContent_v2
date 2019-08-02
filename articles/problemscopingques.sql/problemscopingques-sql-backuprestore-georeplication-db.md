< properties
pageTitle = "Error while Geo-replication"
description = "Scoping questions to capture more details about errors encountered while trying to Geo-replicate SQL DB"
authors = "andikshi"
ms.author = "andikshi"
selfHelpType = "problemScopingQuestions"
supportTopicIds = "32630424"
productPesIds = "13491"
cloudEnvironments = "Public"
schemaVersion = "1"
articleId = "problem-scopingques-sql-backuprestore-georeplication-db" /
	>
#Error when trying to geo - replicate
	-- - {
		"resourceRequired": true,
		"subscriptionRequired": true,
		"formElements": [{
				"id": "problem_start_time",
				"order": 1,
				"controlType": "datetimepicker",
				"displayLabel": "When did the problem start?",
				"infoBalloonText": "Enter the approximate time you started to see the error.",
				"required": true
			},
			{
				"id": "error_dropdown",
				"order": 5,
				"controlType": "dropdown",
				"displayLabel": "source_target_SLO_validation",
				"watermarkText": "Secondry database should always be on the same or higher SLO as compared to the Primary",
				"infoBalloonText": "Select Yes/No",
				"dropdownOptions": [{
						"value": "Yes",
						"text": "Yes"
					},
					{
						"value": "No",
						"text": "No"
					},
					{
						"value": "dont_know_answer",
						"text": "Dont know answer"
					}
				],
				"required": true
			},
			{
				"id": "problem_description",
				"order": 1000,
				"controlType": "multilinetextbox",
				"displayLabel": "Please provide additional context for the error message you are encountering.",
				"required": true,
				"useAsAdditionalDetails": true,
				"watermarkText": "Always provide the full error text from the underlying client library (e.g., SqlClient), not the general error from your client application.  If available, include the client stack trace as well."
			}
		],
		"$schema": "SelfHelpContent"
	}
	-- -