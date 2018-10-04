<properties
         pageTitle="Scoping questions for MARS restore failure"
         description="Scoping questions for MARS restore failure"
         authors="srinathvasireddy"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32553296"
         productPesIds="15207"
         cloudEnvironments="public"
         schemaVersion="1"
		 articleId="171f4f9b-3e04-4b40-8c57-b30b5063c752"
/>
# Questions MARS restore failure
---
{
         "resourceRequired": false,
         "title": "MARS restore failure",
         "fileAttachmentHint": "",
         "formElements": [{
							"id": "os_version",
							"order": 1,
							"controlType": "textbox",
							"displayLabel": "What is the OS version of the impacted system?",
							"watermarkText": "ex. Windows 2012 R2",
							"required": true
					 },{
						 	"id": "machine_name",
							"order": 2,
							"controlType": "textbox",
							"displayLabel": "Which machine is experiencing the problem?",
							"watermarkText": "Enter the name of the Windows Server or Windows Client",
							"required": true
					},{
							"id": "error_message",
							"order": 3,
							"controlType": "textbox",
							"displayLabel": "Provide the error message that are you seeing:",
							"watermarkText": "Copy and paste error message text from failed job details dialog in Microsoft Azure Backup agent",
							"required": true
					},{
						  "id": "get_machineid",
							"order": 4,
							"controlType": "textbox",
							"displayLabel": "Provide the MachineId:",
							"watermarkText": "You can find this information from registry keys HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\Windows Azure Backup\\Config\\MachineId",
							"required": false
					},{
					    "id": "get_resourceId",
							"order": 5,
							"controlType": "textbox",
							"displayLabel": "Provide the ResourceId:",
							"watermarkText": "You can find this information from registry keys HKEY_LOCAL_MACHINE\\SOFTWARE\\Microsoft\\Windows Azure Backup\\Config\\ResourceId",
							"required": false
	 				},{
						 	  "id": "recoverymode_type",
						  	"order": 6,
						  	"controlType": "dropdown",
						  	"displayLabel": "Which type of recovery mode are you performing?",
						  	"watermarkText": "Choose an option",
						  	"dropdownOptions":[{
												"value": "Individual files and folders",
												"text": "Individual files and folders"
											},{
												"value": "Volume",
												"text": "Volume"
											  }
											],
											 "required": false
					},{
							"id": "restore_location",
						  	"order": 7,
						  	"controlType": "dropdown",
						  	"displayLabel": "Which type of restoration are you performing?",
						  	"watermarkText": "Choose an option",
						  	"dropdownOptions":[{
												"value": "Restore data to an alternate machine",
												"text": "Restore data to an alternate machine"
											},{
												"value": "Restore data to the same machine from which the backups were taken",
												"text": "Restore data to the same machine from which the backups were taken"
											  }
											],
											 "required": true
					},{
							"id": "basic_troubleshooting_multiselect",
							"order": 8,
							"controlType": "multiselectdropdown",
							"displayLabel": "Select the troubleshooting steps you have performed:",
							"dropdownOptions": [{
												"value": "Passphrase used for restore and backup are same",
												"text": "Passphrase used for restore and backup are same"
										},{
												"value": "If restoring to alternate machine, then the OS version is same/higher than original",
												"text": "If restoring to alternate machine, then the OS version is same/higher than original"
										},{
												"value": "Machine has Internet connectivity",
												"text": "Machine has Internet connectivity"
										},{
												"value": "Microsoft iSCSI Initiator service is running",
												"text": "Microsoft iSCSI Initiator service is running"
										},{
												"value": "Tried restoring different recovery points",
												"text": "Tried restoring different recovery points"
										  }
									 ],
										"required": true
					},{
							"id": "problem_start_date",
							"order": 9,
							"controlType": "datetimepicker",
							"displayLabel": "When did the problem begin?",
							"required": false
					},{
							"id": "learn_more_text",
							"order": 10,
							"controlType": "infoblock",
							"content": "Please upload all CBEngine log files located at C:\\Program Files\\Microsoft Azure Recovery Services Agent\\Temp. Put all the content to be shared into a single ZIP file and upload the file using 'File upload' on the left."
					}
			]
}
---
