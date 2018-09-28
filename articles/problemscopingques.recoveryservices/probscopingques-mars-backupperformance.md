<properties
         pageTitle="Scoping questions for MARS backup performance"
         description="Scoping questions for MARS backup performance"
         authors="srinathvasireddy"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32553280"
         productPesIds="15207"
         cloudEnvironments="public"
         schemaVersion="1"
		 articleId="a0f92ce4-69a0-48c6-be51-670b7ddcfd16"
/>
# Questions MARS backup performance
---
{
         "resourceRequired": true,
         "title": "MARS backup performance",
         "fileAttachmentHint": "",
         "formElements": [{
						 	"id": "machine_name",
							"order": 1,
							"controlType": "textbox",
							"displayLabel": "Which machine is experiencing the problem?",
							"watermarkText": "Enter the name of the Windows Server or Windows Client",
							"required": true
						},{
						 	"id": "performance_issue_type",
						  	"order": 2,
						  	"controlType": "dropdown",
						  	"displayLabel": "Are you experiencing performance issue with initial/incremental backup?",
						  	"watermarkText": "Choose an option",
						  	"dropdownOptions":[{
												"value": "Initial (first) backup",
												"text": "Initial (first) backup"
											},{
												"value": "Incremental backup",
												"text": "Incremental backup"
											  }
											],
											 "required": true
					 },{
							"id": "agent_location",
						  	"order": 3,
						  	"controlType": "dropdown",
						  	"displayLabel": "Is Azure Backup agent running inside an Azure VM?",
						  	"watermarkText": "Choose an option",
						  	"dropdownOptions":[{
												"value": "Yes",
												"text": "Yes"
											},{
												"value": "No",
												"text": "No"
											  }
											],
											 "required": false
					},{
							"id": "job_time",
							"order": 4,
							"controlType": "textbox",
							"displayLabel": "How long is the backup job running?",
							"watermarkText": "Ex. 18 hrs",
							"required": false
					},{
						    "id": "prerequisites_links",
							"order": 5,
							"controlType": "infoblock",
							"content": "To ensure successful backup, refer to these prerequisites and dependencies:, <a href='https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-slow-backup-performance-issue#cause-another-process-or-antivirus-software-interfering-with-azure-backup'>antivirus prerequisites</a>, <a href='https://docs.microsoft.com/azure/backup/backup-azure-file-folder-backup-faq#what-types-of-drives-can-i-back-up-files-and-folders-from-br'>unsupported drives</a>, and <a href='https://docs.microsoft.com/azure/backup/backup-azure-file-folder-backup-faq#what-file-and-folder-types-can-i-back-up-from-my-serverbr'>unsupported files.</a>"
					},{
							"id": "basic_troubleshooting_multiselect",
							"order": 6,
							"controlType": "multiselectdropdown",
							"displayLabel": "Select the troubleshooting steps you have performed:",
							"dropdownOptions": [{
												"value": "5-10% free volume space is available on scratch folder location",
												"text": "5-10% free volume space is available on scratch folder location"
										},{
												"value": "If antivirus is running, then exclusion rules are used",
												"text": "If antivirus is running, then exclusion rules are used"
										},{
												"value": "Unsupported drives are excluded from backup",
												"text": "Unsupported drives are excluded from backup"
										},{
												"value": "Unsupported files are excluded from backup",
												"text": "Unsupported files are excluded from backup"
										},{
												"value": "Network throttling is not configured on the machine",
												"text": "Network throttling is not configured on the machine"
										}
									 ],
										"required": true
					},{
							"id": "learn_more_text",
							"order": 7,
							"controlType": "infoblock",
							"content": "Please upload all CBEngine log files located at C:\\Program Files\\Microsoft Azure Recovery Services Agent\\Temp. Put all the content to be shared into a single ZIP file and upload the file using 'File upload' on the left."
					}
			]
}
---
