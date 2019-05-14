<properties
         pageTitle="Scoping questions for DPM Online backup is failing"
         description="Scoping questions for DPM Online backup is failing"
         authors="srinathvasireddy"
	 ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32553293"
         productPesIds="15207"
         cloudEnvironments="public"
         schemaVersion="1"
	 articleId="229892a8-0d21-433a-90cd-a32f8ec9abd8"
/>
# Questions DPM - Online backup is failing
---
{
         "resourceRequired": true,
	 "subscriptionRequired": true,
         "title": "DPM Online backup is failing",
         "fileAttachmentHint": "",
         "formElements": [{
			  "id": "issue_Type",
			  "visibility": "null",
                          "order": 1,
                          "controlType": "dropdown",
			  "displayLabel": "Backups are failing to the disk or cloud?",
                          "watermarkText": "Select",
			  "dropdownOptions":[{
						"value": "Backups to the cloud are failing",
						"text": "Backups to the cloud are failing"
					},{
						"value": "Backups to the disk are failing",
						"text": "Backups to the disk are failing"
					},{
						"value": "dont_know_answer",
						"text": "Other, don't know or not applicable"
						}
				],
				 "required": true
			},{
			  "id": "os_version",
                          "order": 2,
			  "visibility": "issue_Type == Backups to the cloud are failing",
                          "controlType": "textbox",
                          "displayLabel": "What is the OS version of the impacted Server?",
                          "watermarkText": "ex. Windows 2012 R2",
                          "required": true
                        },{
		   	"id": "machine_name",
			"order": 3,
			"visibility": "issue_Type == Backups to the cloud are failing",
			"controlType": "textbox",
			"displayLabel": "Which machine is experiencing the problem?",
			"watermarkText": "Enter the name of the impacted machine",
			"required": false
                        },{
		    	"id": "backup_type",
			"order": 4,
			"visibility": "issue_Type == Backups to the cloud are failing",
			"controlType": "dropdown",
			"displayLabel": "Is this an initial/incremental backup failure?",
			"watermarkText": "Select",
			"dropdownOptions": [{
						"value": "Initial backup failure",
						"text": "Initial backup failure"
					},{
						"value": "Incremental backup failure",
						"text": "Incremental backup failure"
					},{
						"value": "dont_know_answer",
						"text": "Other, don't know or not applicable"
					}
				],
				"required": true
			},{
		    	"id": "error_message",
			"order": 5,
			"visibility": "issue_Type == Backups to the cloud are failing || issue_Type == Backups to the disk are failing",
			"controlType": "textbox",
			"displayLabel": "Provide the error message that you are seeing:",
			"watermarkText": "Copy and paste error message text from the console instead of screenshot",
			"required": false
			},{
                          "id": "workload_Type",
			  "visibility": "issue_Type == Backups to the cloud are failing",
                          "order": 6,
                          "controlType": "dropdown",
			  "displayLabel": "Which type of data source you are backing up?",
                          "watermarkText": "Select workload type",
			  "dropdownOptions":[{
					    "value": "files and folder",
					    "text": "files and folder"
					},{
					    "value": "dont_know_answer",
					    "text": "Other, don't know or not applicable"
					}
				],
				"required": true
			},{
			"id": "Basic_troubleshooting_multiselect",
			"order": 7,
			"visibility": "issue_Type == Backups to the cloud are failing",
			"controlType": "multiselectdropdown",
			"infoBalloonText": "Check System Center DPM <a href='https://aka.ms/AB-DPM-tshooting'>Troubleshooting</a> article",
			"displayLabel": "Select the troubleshooting steps that you have performed:",
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
					},{
						"value": "dont_know_answer",
						"text": "Other, don't know or not applicable"
					}
				],
					"required": false
                        },{
                            	"id": "get_machineid",
				"order": 8,
				"visibility": "issue_Type == Backups to the cloud are failing",
				"controlType": "textbox",
				"displayLabel": "Provide the MachineId:",
				"infoBalloonText": "Find MachineId from registry HKEY_LOCAL_MACHINE\\\\SOFTWARE\\\\Microsoft\\\\Windows Azure Backup\\\\Config\\\\MachineId",
				"watermarkText": "Paste MachineId here",
				"required": false
		    },{
				"id": "get_resourceId",
				"order": 9,
				"visibility": "issue_Type == Backups to the cloud are failing",
				"controlType": "textbox",
				"displayLabel": "Provide the ResourceId:",
				"infoBalloonText": "Find ResourceId from registry HKEY_LOCAL_MACHINE\\\\SOFTWARE\\\\Microsoft\\\\Windows Azure Backup\\\\Config\\\\ResourceId",
				"watermarkText": "Paste ResourceId here",
				"required": false
                        },{
				"id": "problem_start_time",
				"order": 10,
				"visibility": "null",
				"controlType": "datetimepicker",
				"displayLabel": "When did the problem begin?",
				"required": true
                        },{
				  "id": "problem_description",
				  "order": 11,
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
