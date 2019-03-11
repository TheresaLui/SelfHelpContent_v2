<properties
         pageTitle="Scoping questions for SQL database configuration failure"
         description="Scoping questions for SQL database configuration failure"
         authors="srinathvasireddy"
	 ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32605793"
         productPesIds="15207"
         cloudEnvironments="public"
         schemaVersion="1"
         articleId="fbf623da-eef7-4edc-b642-b63859051ee6"
/>
# Questions SQL database configuration failure
---
{
		 "resourceRequired": true,
		 "title": "SQL database configuration failure",
		 "fileAttachmentHint": "",
		 "formElements": [{
					"id": "machine_name",
					"order": 1,
					"visibility": "null",
					"controlType": "textbox",
					"displayLabel": "Which machine is experiencing the problem?",
					"watermarkText": "Enter the name of the virtual machine running SQL",
					"required": true
				},{
					"id": "os_version",
					"order": 2,
					"visibility": "null",
					"controlType": "textbox",
					"displayLabel": "What is the OS version of the machine?",
					"watermarkText": "ex. Windows Server 2012 R2",
					"required": true
				},{
					"id": "sql_version",
					"order": 3,
					"visibility": "null",
					"controlType": "textbox",
					"displayLabel": "What is the SQL Server version and edition?",
					"watermarkText": "ex. SQL Server 2012 Standard",
					"required": true
				},{
					"id": "database_Name",
					"order": 4,
					"visibility": "null",
					"controlType": "textbox",
					"displayLabel": "Provide the name(s) of the databases whose configuration is failing",
					"watermarkText": "Enter database name(s) separated by comma",
					"required": true
				},{
					"id": "config_Type",
					"order": 5,
					"visibility": "null",
					"controlType": "dropdown",
					"displayLabel": "At what stage of setup are you experiencing this failure?",
					"watermarkText": "Select",
					"dropdownOptions": [{
								"value": "Start Discovery",
								"text": "Start Discovery"
				},{
								"value": "Discover DBs",
								"text": "Discover DBs"
				},{
								"value": "Configure Backup",
								"text": "Configure Backup"
				}
				],
				"required": true
				},{
					"id": "jobID_Name",
					"order": 6,
					"visibility": "config_Type == Configure Backup",
					"controlType": "textbox",
					"displayLabel": "Enter the failed configuration job Activity ID:",
					"watermarkText": "Ex. cace7461-dd3c-4e38-b4db-38dc57fdee7b",
					"required": false
				},{
					"id": "error_message",
					"order": 7,
					"visibility": "null",
					"controlType": "textbox",
					"displayLabel": "Provide the error message that are you seeing:",
					"watermarkText": "Copy and paste the error message details",
					"required": true
				},{
					"id": "basic_troubleshooting_multiselect",
					"order": 8,
					"visibility": "null",
					"controlType": "multiselectdropdown",
					"displayLabel": "Select the troubleshooting steps you have performed:",
					"dropdownOptions": [{
								"value": "Checked OS version is supported for backup",
								"text": "Checked OS version is supported for backup"
							},{
								"value": "Checked SQL version and edition are supported for backup",
								"text": "Checked SQL version and edition are supported for backup"
							},{
								"value": "Checked the Machine has Internet connectivity",
								"text": "Checked the Machine has Internet connectivity"
							},{
								"value": "Checked the SQL Server VM has required permission for backup",
								"text": "Checked the SQL Server VM has required permission for backup"
							}
						],
						"required": true
				},{
					"id": "problem_start_time",
					"order": 9,
					"visibility": "null",
					"controlType": "datetimepicker",
					"displayLabel": "When did the problem begin?",
					"required": true
				},{
					"id": "problem_description",
					"order": 10,
					"controlType": "multilinetextbox",
					"useAsAdditionalDetails": true,
					"displayLabel": "Additional details:",
					"watermarkText": "Provide additional information about your issue",
					"required": true,
					"hints": []
			}
            ]
}
---
