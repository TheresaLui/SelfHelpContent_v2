<properties
         pageTitle="Scoping questions for System State restore performance"
         description="Scoping questions for System State restore performance"
         authors="srinathvasireddy"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32632800"
         productPesIds="15207"
         cloudEnvironments="public"
         schemaVersion="1"
	 articleId="9182b0e1-cf2a-48a6-9b3d-9a4ae08bcf86"
/>
# Questions System State restore performance
---
{
         "resourceRequired": true,
	 "subscriptionRequired": true,
         "title": "System State restore performance",
         "fileAttachmentHint": "",
         "formElements": [{
			"id": "machine_name",
			"order": 1,
			"controlType": "textbox",
			"displayLabel": "Which machine is experiencing the problem?",
			"watermarkText": "Enter the name of the Windows Server or Windows Client",
			"required": false
		},{
			"id": "restore_type",
			"order": 2,
			"controlType": "dropdown",
			"displayLabel": "Which type of restoration are you performing?",
			"watermarkText": "Select",
			"dropdownOptions":[{
					"value": "Restore data to an alternate machine.",
					"text": "Restore data to an alternate machine."
				},{
					"value": "Restore data to the same machine from which the backups were taken",
					"text": "Restore data to the same machine from which the backups were taken"
				  }
				],
				 "required": true
		},{
			"id": "job_time",
			"order": 4,
			"controlType": "textbox",
			"displayLabel": "How long is the restore job is running?",
			"watermarkText": "Ex. 18 hrs",
			"required": false
		},{
			  "id": "problem_start_time",
			  "order": 5,
			  "controlType": "datetimepicker",
			  "displayLabel": "When did the problem begin?",
			  "required": true
		},{
			  "id": "problem_description",
			  "order": 6,
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
