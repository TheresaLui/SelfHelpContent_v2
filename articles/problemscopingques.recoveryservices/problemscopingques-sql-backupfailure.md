<properties
         pageTitle="Scoping questions for SQL database backup failure"
         description="Scoping questions for SQL database backup failure"
         authors="srinathvasireddy"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32605791"
         productPesIds="15207"
         cloudEnvironments="public"
         schemaVersion="1"
	 articleId="d73dbe86-4f8e-414d-8963-7d22d012b671"
/>
# Questions SQL database backup failure
---
{
         "resourceRequired": true,
         "title": "SQL database backup failure",
         "fileAttachmentHint": "",
         "formElements": [{
							"id": "machine_name",
							"order": 1,
							"controlType": "textbox",
							"displayLabel": "Which SQL machine is experiencing the problem?",
							"watermarkText": "Enter the name of the SQL virtual machine",
							"required": true
					 },{
							"id": "os_version",
							"order": 2,
							"controlType": "textbox",
							"displayLabel": "What is the os version of impacted SQL machine?",
							"watermarkText": "ex. Windows Server 2012 R2",
							"required": true
					 },{
							"id": "sql_version",
							"order": 3,
							"controlType": "textbox",
							"displayLabel": "What is the SQL server version and edition of impacted machine?",
							"watermarkText": "ex. SQL Server 2012 Standard",
							"required": true
					 },{
							"id": "database_Name",
							"order": 4,
							"controlType": "textbox",
							"displayLabel": "Which database backup is failing?",
							"watermarkText": "Enter the name of the databases you are unable to backup",
							"required": true
					 },{
							"id": "backup_Type",
							"order": 5,
							"controlType": "dropdown",
							"displayLabel": "Is it Full/Log/Differential backup failure?",
							"watermarkText": "Select",
							"dropdownOptions": [{
													"value": "Full backup",
													"text": "Full backup"
												},{
													"value": "Log backup",
													"text": "Log backup"
												},{
													"value": "Differential backup",
													"text": "Differential backup"
												}
						  						],
													"required": true
					 },{
							"id": "JobID_Name",
							"order": 6,
							"controlType": "textbox",
							"displayLabel": "Enter the failed backup job Activity ID",
							"watermarkText": "Enter the failed backup Job Activity ID that is experiencing the problem",
							"required": true
					 },{
							"id": "learn_more_text",
							"order": 7,
							"controlType": "infoblock",
							"content": "Microsoft can provide a solution to your problem faster if you can provide a failed Backup Job Activity ID. From a new browser tab, you can find this from Recovery Services Vault > Monitoring and Report > Backup Jobs > Failed > Activity ID."
					 },{
							"id": "error_message",
							"order": 8,
							"controlType": "textbox",
							"displayLabel": "Provide the error message that are you seeing:",
							"watermarkText": "Copy and paste the error message here that are you seeing",
							"required": true
					},{
							"id": "prerequisites_links",
							"order": 9,
							"controlType": "infoblock",
							"content": "To ensure SQL database successful backup, refer to these prerequisites and dependencies:, <a href='https://docs.microsoft.com/azure/backup/backup-azure-sql-database#supported-operating-systems'>supported OS version</a>, <a href='https://docs.microsoft.com/azure/backup/backup-azure-sql-database#supported-sql-server-versions-and-editions'>supported SQL server versions and editions</a>, <a href='https://docs.microsoft.com/azure/backup/backup-azure-sql-database#prerequisites'>permission required on VM.</a>"
					},{
							"id": "basic_troubleshooting_multiselect",
							"order": 10,
							"controlType": "multiselectdropdown",
							"displayLabel": "Select the troubleshooting steps you have performed:",
							"dropdownOptions": [{
												"value": "OS version is supported for backup",
												"text": "OS version is supported for backup"
										},{
												"value": "SQL version and edition are supported for backup",
												"text": "SQL version and edition are supported for backup"
										},{
												"value": "Machine has Internet connectivity",
												"text": "Machine has Internet connectivity"
										},{
												"value": "SQL server vm has required permission for backup",
												"text": "SQL server vm has required permission for backup"
										}
									],
										"required": true
					  },{
							"id": "problem_start_date",
							"order": 11,
							"controlType": "datetimepicker",
							"displayLabel": "When did the problem begin?",
							"required": false
					 },{
							"id": "learn_more_text1",
							"order": 12,
							"controlType": "infoblock",
							"content": "Please upload SQL Server logs located at default installation path C:\\\\Program Files\\\\Microsoft SQL Server\\\\MSSQL11.MSSQLSERVER\\\\MSSQL\\\\Log. Put all the content to be shared into a single ZIP file and upload the file using 'File upload' on the left."
					}
			]
}
---
