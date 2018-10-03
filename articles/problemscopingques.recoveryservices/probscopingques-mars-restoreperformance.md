<properties
         pageTitle="Scoping questions for MARS restore performance"
         description="Scoping questions for MARS restore performance"
         authors="srinathvasireddy"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32613000"
         productPesIds="15207"
         cloudEnvironments="public"
         schemaVersion="1"
	 articleId="9434ba9d-5881-4eea-8c68-6b3cde03323e"
/>
# Questions MARS restore performance
---
{
         "resourceRequired": true,
         "title": "MARS restore performance",
         "fileAttachmentHint": "",
         "formElements": [{
							"id": "machine_name",
							"order": 1,
							"controlType": "textbox",
							"displayLabel": "Which machine is experiencing the problem?",
							"watermarkText": "Enter the name of the Windows Server or Windows Client",
							"required": true
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
							"id": "recoverymode_type",
						  	"order": 3,
						  	"controlType": "dropdown",
						  	"displayLabel": "Which type of recovery mode are you performing?",
						  	"watermarkText": "Select",
						  	"dropdownOptions":[{
												"value": "Individual files and folders",
												"text": "Individual files and folders"
											},{
												"value": "Volume",
												"text": "Volume"
											  }
											],
											 "required": true
					},{
							"id": "job_time",
							"order": 4,
							"controlType": "textbox",
							"displayLabel": "How long is the restore job running?",
							"watermarkText": "Ex. 18 hrs",
							"required": true
					},{
							"id": "learn_more_text",
							"order": 5,
							"controlType": "infoblock",
							"content": "Please upload all CBEngine log files located at C:\\Program Files\\Microsoft Azure Recovery Services Agent\\Temp. Put all the content to be shared into a single ZIP file and upload the file using 'File upload' on the left."
					}
			]
}
---
