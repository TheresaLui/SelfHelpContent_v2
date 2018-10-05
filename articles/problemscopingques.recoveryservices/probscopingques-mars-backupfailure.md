<properties
         pageTitle="Scoping questions for MARS backup failure"
         description="Scoping questions for MARS backup failure"
         authors="srinathvasireddy"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32553275"
         productPesIds="15207"
         cloudEnvironments="public"
         schemaVersion="1"
	 articleId="9e7d5d78-5ea7-4985-ac04-19ee33642d4d"
/>
# Questions MARS backup failure
---
{
         "resourceRequired": false,
         "title": "MARS backup failure",
         "fileAttachmentHint": "",
         "formElements":[{
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
							"id": "backup_type",
							"order": 3,
							"controlType": "dropdown",
							"displayLabel": "Is this an initial/incremental backup failure?",
							"watermarkText": "Select",
							"dropdownOptions": [{
							  						"value": "Initial backup failure",
							  						"text": "Initial backup failure"
												},{
							   						"value": "Incremental backup failure",
							   						"text": "Incremental backup failure"
												  }
												],
												"required": true
					},{
					  	 	"id": "error_message",
							"order": 4,
							"controlType": "textbox",
							"displayLabel": "Provide the error message that are you seeing:",
							"watermarkText": "Copy and paste error message text from failed job details dialog in Microsoft Azure Backup agent",
							"required": true
					},{
						    "id": "prerequisites_links",
							"order": 5,
							"controlType": "infoblock",
							"content": "To ensure successful backup, refer to these prerequisites and dependencies:, <a href='http://aka.ms/azurebackup_agent'>latest Azure Backup agent</a>, <a href='https://docs.microsoft.com/azure/backup/backup-configure-vault#network-and-connectivity-requirements'>whitelist URLs on firewall</a>, <a href='https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-slow-backup-performance-issue#cause-another-process-or-antivirus-software-interfering-with-azure-backup'>antivirus prerequisites</a>, <a href='https://docs.microsoft.com/azure/backup/backup-azure-file-folder-backup-faq#what-types-of-drives-can-i-back-up-files-and-folders-from-br'>unsupported drives</a>, and <a href='https://docs.microsoft.com/azure/backup/backup-azure-file-folder-backup-faq#what-file-and-folder-types-can-i-back-up-from-my-serverbr'>unsupported files.</a>"
					},{
							"id": "basic_troubleshooting_multiselect",
							"order": 6,
							"controlType": "multiselectdropdown",
							"displayLabel": "Select the troubleshooting steps you have performed:",
							"dropdownOptions": [{
													"value": "Azure Backup agent is latest",
													"text": "Azure Backup agent is latest"
												},{
													"value": "Firewall settings on the machine/proxy are configured to allow the required URLs",
													"text": "Firewall settings on the machine/proxy are configured to allow the required URLs"
						 						},{
													"value": "Machine has Internet connectivity",
													"text": "Machine has Internet connectivity"
						 						},{
													"value": "5-10% free volume space is available on scratch folder location",
													"text": "5-10% free volume space is available on scratch folder location"
												},{
													"value": "If antivirus is running, then exclusion rules are used",
													"text": "If antivirus is running, then exclusion rules are used"
						 						},{
													"value": "Proxy is enabled",
													"text": "Proxy is enabled"
												},{
													"value": "Unsupported drives are excluded from backup",
													"text": "Unsupported drives are excluded from backup"
												},{
													"value": "Unsupported files are excluded from backup",
													"text": "Unsupported files are excluded from backup"
												  }
						  						],
													"required": true
					},{
					        "id": "get_machineid",
							"order": 7,
							"controlType": "textbox",
							"displayLabel": "Provide the MachineId:",
							"watermarkText": "You can find this information from registry keys HKEY_LOCAL_MACHINE\\\\SOFTWARE\\\\Microsoft\\\\Windows Azure Backup\\\\Config\\\\MachineId",
							"required": false
					},{
							"id": "get_resourceId",
							"order": 8,
							"controlType": "textbox",
							"displayLabel": "Please provide the ResourceId:",
							"watermarkText": "You can find this information from registry keys HKEY_LOCAL_MACHINE\\\\SOFTWARE\\\\Microsoft\\\\Windows Azure Backup\\\\Config\\\\ResourceId",
							"required": false
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
							"content": "Please upload all CBEngine log files located at C:\\\\Program Files\\\\Microsoft Azure Recovery Services Agent\\\\Temp. Put all the content to be shared into a single ZIP file and upload the file using 'File upload' on the left."
					  }
		]
}
---
