<properties
         pageTitle="Scoping questions for MARS Installation or registration failure"
         description="Scoping questions for MARS Installation or registration failure"
         authors="srinathvasireddy"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32553287"
         productPesIds="15207"
         cloudEnvironments="public"
         schemaVersion="1"
	 articleId="0d4bc270-b32b-49f9-8b5c-c6d01db47adf"
/>
# Questions MARS Installation or registration failure
---
{
         "resourceRequired": true,
         "title": "MARS Installation or registration failure",
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
							"id": "registration_type",
							"order": 4,
							"controlType": "dropdown",
							"displayLabel": "Is this an intial-registration/re-registering issue?",
							"watermarkText": "Select",
							"dropdownOptions": [{
							  						"value": "Initial-registration",
							  						"text": "Initial-registration"
					  							},{
							   						"value": "Re-registering",
							   						"text": "Re-registering"
					   							}
					   							],
													"required": true
					},{
							"id": "infoblock_reregistration",
							"order": 5,
							"visiblity": "registration_type == re-registering",
							"controlType": "infoblock",
							"content": "Note: To re-register machine to the same vault, use the same passphrase that was used during initial registration."
					},{
							"id": "prerequisites_links",
							"order": 6,
							"controlType": "infoblock",
							"content": "To ensure successful installation and configuration, refer to these prerequisites and dependencies: <a href='https://docs.microsoft.com/azure/backup/backup-azure-backup-faq#which-operating-systems-does-azure-backup-support-br'>supported OS</a>, <a href='https://docs.microsoft.com/azure/backup/backup-configure-vault#network-and-connectivity-requirements'>whitelist URLs on firewall</a>, <a href='https://www.microsoft.com/download/details.aspx?id=53345'>.net framework version requirements</a>, and <a href='https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-slow-backup-performance-issue#cause-another-process-or-antivirus-software-interfering-with-azure-backup'>antivirus prerequisites.</a>"
					},{
							"id": "basic_troubleshooting_multiselect",
							"order": 7,
							"controlType": "multiselectdropdown",
							"displayLabel": "Select the troubleshooting steps you have performed:",
							"dropdownOptions": [{
												"value": "OS version is supported for backup",
												"text": "OS version is supported for backup"
										},{
												"value": "If firewall is used, then required URLs are whitelisted",
												"text": "If firewall is used, then required URLs are whitelisted"
										},{
												"value": "Machine has Internet connectivity",
												"text": "Machine has Internet connectivity"
										},{
												"value": "If antivirus is running, then exclusion rules are used",
												"text": "If antivirus is running, then exclusion rules are used"
										},{
												"value": ".NET framework version is at least 4.6.2",
												"text": ".NET framework version is at least 4.6.2"
										},{
												"value": "Server is not registered with another vault",
												"text": "Server is not registered with another vault"
										},{
										  		"value": "Ensure c:/windows/temp folder has less than 60,000 files",
												"text": "Ensure c:/windows/temp folder has less than 60,000 files"
										}
									],
										"required": true			
					  }
			]
}
---
