<properties
         pageTitle="Scoping questions for Azure backup server Installation or Configuration Failures"
         description="Scoping questions for Azure backup server Installation or Configuration Failures"
         authors="srinathvasireddy"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32570754"
         productPesIds="15207"
         cloudEnvironments="public"
         schemaVersion="1"
	 articleId="26a0819f-c924-4d9a-9735-818aac4dc67e"
/>
# Questions Azure backup server - Installation or Configuration Failures
---
{
         "resourceRequired": true,
         "title": "Azure backup server Installation or Configuration Failures",
         "fileAttachmentHint": "",
         "formElements": [{
         			"id": "installation_Type",
				"visibility": "null",
         			"order": 1,
        			"controlType": "dropdown",
         			"displayLabel": "Is this a new/upgrade installation?",
         			"watermarkText": "Select",
				"dropdownOptions":[{
				  	    		"value": "New",
					  		"text": "New"
						  },{
							"value": "Upgrade from V1 to V2",
							"text": "Upgrade from V1 to V2"
						  }
						],
						"required": true
			},{
				"id": "issue_Type",
				"visibility": "installation_Type == New",
                 		"order": 2,
                 		"controlType": "dropdown",
                 		"displayLabel": "At what point is the installation failing?",
                 		"watermarkText": "Select",
				"dropdownOptions":[{
						    "value": "Microsoft Azure Recovery Service agents failed to install",
						    "text": "Microsoft Azure Recovery Service agents failed to install"
					},{
						     "value": "SQL components failed to install",
						     "text": "SQL components failed to install"
					},{
						    "value": "Microsoft Azure backup(DPM) software failed to install",
						    "text": "Microsoft Azure backup(DPM) software failed to install
					}
				  ],
				     "required": true
			},{
				"id": "os_version",
				"order": 3,
				"visibility": "issue_Type == Microsoft Azure Recovery Service agents failed to install || issue_Type == SQL components failed to install || issue_Type == Microsoft Azure backup(DPM) software failed to install",
				"controlType": "textbox",
				"displayLabel": "What is the OS version of the dedicated server?",
				"watermarkText": "ex. Windows 2012 R2",
				"required": true
			},{
				"id": "registration_Type",
				"order": 4,
				"visibility": "issue_Type == Microsoft Azure Recovery Service agents failed to install",
				"controlType": "dropdown",
				"displayLabel": "Is this an initial-registration/re-registration issue?",
				"watermarkText": "Select",
				"dropdownOptions": [{
							  "value": "Initial-registration",
							  "text": "Initial-registration"
					  },{
							   "value": "Re-registration",
							   "text": "Re-registration"
					 	}
					   	],
						"required": false
					  },{
				"id": "prerequisites_links",
				"order": 5,
				"controlType": "infoblock",
				"content": "To ensure successful installation and configuration, refer to these prerequisites and dependencies: <a href='https://docs.microsoft.com/azure/backup/backup-azure-backup-faq#which-operating-systems-does-azure-backup-support-br'>supported OS</a>, <a href='https://docs.microsoft.com/azure/backup/backup-configure-vault#network-and-connectivity-requirements'>whitelist URLs on firewall</a>, <a href='https://www.microsoft.com/download/details.aspx?id=53345'>.net framework version requirements</a>, and <a href='https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-slow-backup-performance-issue#cause-another-process-or-antivirus-software-interfering-with-azure-backup'>antivirus prerequisites.</a>"		
					},{
				"id": "basic_troubleshooting_multiselect",
				"order": 6,
				"visibility": "issue_Type == Microsoft Azure Recovery Service agents failed to install",
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
				},{
              						"id": "learn_more_text1",
							"order": 7,
							"visibility": "issue_Type == Microsoft Azure Recovery Service agents failed to install || issue_Type == SQL components failed to install || issue_Type == Microsoft Azure backup(DPM) software failed to install",
							"controlType": "infoblock",
				       			"content": "Installation of Azure Backup Server on a domain controller is not supported, <a href='https://docs.microsoft.com/azure/backup/backup-mabs-install-azure-stack#using-an-iaas-vm-in-azure-stack'>learn more</a>."
          			},{
              						"id": "learn_more_text2",
							"order": 8,
							"visibility": "issue_Type == Microsoft Azure Recovery Service agents failed to install || issue_Type == SQL components failed to install || issue_Type == Microsoft Azure backup(DPM) software failed to install",
							"controlType": "infoblock",
							"content": "Please upload  DPMSetup.txt file located at "C:\\\\Program Files\\\\Microsoft Azure Backup Server\\\\DPM\\\\DPMLogs\\\\" using 'File upload' on the left."
				},{
							"id": "error_message",
							"order": 9,
							"controlType": "textbox",
							"displayLabel": "Provide the error message that are you seeing:",
							"watermarkText": "Copy and paste error message text from the console",
							"required": true
					}
				]}
---
