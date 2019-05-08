<properties
         pageTitle="Scoping questions for Azure File Share restore performance issue"
         description="Scoping questions for Azure File Share restore performance issue"
         authors="srinathvasireddy"
		     ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32612215"
         productPesIds="15207"
         cloudEnvironments="public"
         schemaVersion="1"
		     articleId="715505fa2-821e-4988-8b3d-d160e70e6ac9"
/>
# Questions for Azure File Share restore performance issue
---
{
         "resourceRequired": true,
		     "subscriptionRequired": true,
         "title": "Azure File Share restore performance issue",
         "fileAttachmentHint": "",
         "formElements": [{
							"id": "storage_account_name",
							"order": 1,
							"controlType": "textbox",
							"displayLabel": "Which storage account(s) is experiencing the problem?",
							"watermarkText": "Enter the name of the storage account(s)",
							"required": false
						},{
							"id": "fileshare_Name",
							"order": 2,
							"controlType": "textbox",
							"displayLabel": "Provide the name(s) of the File Share for which you are facing performance issue:",
							"watermarkText": "Enter file share name(s) comma separated",
							"required": false
							
						},{	
							"id": "restore_Type",
							"order": 3,
							"controlType": "dropdown",
							"displayLabel": "Which type of restore you are performing?",
							"watermarkText": "Select",
							"dropdownOptions": [{
												"value": "Original Location",
												"text": "Original Location"
								},{
												"value": "Alternate Location",
												"text": "Alternate Location"
								},{
												"value": "dont_know_answer",
												"text": "Other, don't know or not applicable"
								}
								],
								"required": true
					},{
							"id": "JobID_Name",
							"order": 4,
							"controlType": "textbox",
							"displayLabel": "Enter the long running job activity ID:",
							"watermarkText": "Ex. cace7461-dd3c-4e38-b4db-38dc57fdee7b",
							"required": false
					},{
							"id": "job_Running_Time",
							"order": 5,
							"controlType": "textbox",
							"displayLabel": "Since how long the job is running?",
							"watermarkText": "Enter time in hours ex. 18hrs",
							"required": false
					},{
							"id": "problem_description",
							"order": 6,
							"controlType": "multilinetextbox",
							"useAsAdditionalDetails": true,
							"displayLabel": "Additional details",
							"watermarkText": "Provide additional information about your issue",
							"required": true,
							"hints": []
					},{
							"id": "problem_start_time",
							"order": 7,
							"controlType": "datetimepicker",
							"displayLabel": "Problem start time",
							"required": true
		}
	]
}
---
