<properties
         pageTitle="Scoping questions for SQL restore performance"
         description="Scoping questions for SQL restore performance"
         authors="srinathvasireddy"
		 ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32605796"
         productPesIds="15207"
         cloudEnvironments="public"
         schemaVersion="1"
         articleId="ac52a26c-bb4f-4dc5-bfb1-0bfd0ea9b489"
/>
# Questions SQL database restore performance
---
{
   "resourceRequired": true,
	 "subscriptionRequired": true,
	 "title": "SQL database restore performance",
	 "fileAttachmentHint": "",
	 "formElements": [{
			"id": "machine_name",
			"order": 1,
			"controlType": "textbox",
			"displayLabel": "Which machine is experiencing the problem?",
			"watermarkText": "Enter the name of the virtual machine running SQL",
			"required": false
		}, {
			"id": "database_Name",
			"order": 2,
			"controlType": "textbox",
			"displayLabel": "Provide the name(s) of the databases whose restore is slow?",
			"watermarkText": "Enter database name(s) comma separated",
			"required": false
		}, {
			"id": "restore_Type",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "Which type of restore are you performing?",
			"watermarkText": "Select",
			"dropdownOptions": [{
					"value": "Alternate Location",
					"text": "Alternate Location"
				}, {
					"value": "Overwrite DB",
					"text": "Overwrite DB"
				}, {
					"value": "dont_know_answer",
					"text": "Other, don't know or not applicable"
				}
			],
			"required": true
		}, {
			"id": "restore_Type1",
			"order": 4,
			"controlType": "dropdown",
			"displayLabel": "Which type of performance issue are you facing",
			"watermarkText": "Select",
			"dropdownOptions": [{
					"value": "Slow restore during Logs (Point in Time) restore operation",
					"text": "Slow restore during Logs (Point in Time) restore operation"
				}, {
					"value": "Slow restore during Full & Differential restore operation",
					"text": "Slow restore during Full & Differential restore operation"
				}, {
					"value": "dont_know_answer",
					"text": "Other, don't know or not applicable"
				}
			],
			"required": true
		}, {
			"id": "jobID_Name",
			"order": 5,
			"controlType": "textbox",
			"displayLabel": "Enter the long running job activity ID:",
			"watermarkText": "Ex. cace7461-dd3c-4e38-b4db-38dc57fdee7b",
			"required": false
			
		},{
      "id": "job_Running_Time",
      "order": 6,
      "controlType": "textbox",
      "displayLabel": "Since how long the job is running?",
      "watermarkText": "Enter time in hours ex. 18hrs",
      "required": false
        },{
			"id": "problem_start_time",
			"order": 7,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": true
		}, {
			"id": "problem_description",
			"order": 8,
			"controlType": "multilinetextbox",
			"useAsAdditionalDetails": true,
			"displayLabel": "Additional details",
			"watermarkText": "Provide additional information about your issue",
			"required": true,
			"hints": []
		 }
	]
}
---
