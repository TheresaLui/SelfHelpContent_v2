<properties
         pageTitle="Scoping questions for Azure File Share restore performance issue"
         description="Scoping questions for Azure File Share restore performance issue"
         authors="srinathv"
	 ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32612215"
         productPesIds="15207"
         cloudEnvironments="public"
         schemaVersion="1"
	 articleId="715505fa2-821e-4988-8b3d-d160e70e6ac9"
/>
# Questions for Azure File Share restore performance issue
---
{
         "resourceRequired": true,
	 "subscriptionRequired": true,
         "title": "Azure File Share restore performance issue",
         "fileAttachmentHint": "",
	"formElements": [{
			"id": "storage_account_name",
			"order": 1,
			"controlType": "textbox",
			"displayLabel": "Which storage account(s) is experiencing the problem?",
			"watermarkText": "Enter the name of the storage account(s)",
			"required": false
		},{
			"id": "fileshare_Name",
			"order": 2,
			"controlType": "textbox",
			"displayLabel": "Provide the name(s) of the File Share for which you are facing performance issue:",
			"watermarkText": "Enter file share name(s) comma separated",
			"required": false
		},{
			"id": "restore_Type",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "Which type of restore you are performing?",
			"watermarkText": "Select",
			"dropdownOptions": [{
					"value": "Original Location",
					"text": "Original Location"
				},{
					"value": "Alternate Location",
					"text": "Alternate Location"
				},{
					"value": "dont_know_answer",
					"text": "Other, don't know or not applicable"
				}
			],
			"required": true
	},{
			"id": "JobID_Name",
			"order": 4,
			"controlType": "textbox",
			"displayLabel": "Enter the long running job activity ID:",
			"watermarkText": "Ex. cace7461-dd3c-4e38-b4db-38dc57fdee7b",
			"required": false
	},{
			"id": "Data_types",
			"order": 5,
			"controlType": "dropdown",
			"infoBalloonText": "Note: Restore time is proportional to the number of files",
			"displayLabel": "Which type of data is present in Azure File share?",
			"watermarkText": "Select"
			"dropdownOptions": [{
					"value": "Large number of small files",
					"text": "Large number of small files"
				},{
					"value": "Small number of Large file",
					"text": "Small number of Large files"
				},{
					"value": "dont_know_answer",
					"text": "Other, don't know or not applicable"
				}
			],
			"required": true
	},{
			"id": "Data_hierarchy",
			"order": 6,
			"controlType": "dropdown",
			"infoBalloonText": "Note: If there are more number of directories, restore is expected to be slower",
			"displayLabel": "How is the directory to file ratio in Azure File share?",
			"watermarkText": "Select"
			"dropdownOptions": [{
					"value": "More directories",
					"text": "More directories"
				},{
					"value": "Less directories",
					"text": "Less directories"
				},{
					"value": "dont_know_answer",
					"text": "Other, don't know or not applicable"
				}
			],
			"required": true
	},{
			"id": "Share_use_status",
			"order": 7,
			"controlType": "dropdown",
			"infoBalloonText": "Note: If other applications are consuming File share IOPS then restore is expected to be slower",
			"displayLabel": "Are other applications using the same File share?",
			"watermarkText": "Select"
			"dropdownOptions": [{
					"value": "Yes",
					"text": "Yes"
			},{
					"value": "No",
					"text": "No"
			},{
					"value": "dont_know_answer",
					"text": "Other, don't know or not applicable"
			}
		],
		"required": true
	},{
			"id": "job_Running_Time",
			"order": 7,
			"controlType": "textbox",
			"displayLabel": "Since how long the job is running?",
			"watermarkText": "Enter time in hours ex. 18hrs",
			"required": false
	},{
			"id": "problem_description",
			"order": 8,
			"controlType": "multilinetextbox",
			"useAsAdditionalDetails": true,
			"displayLabel": "Additional details",
			"watermarkText": "Provide additional information about your issue",
			"required": true,
			"hints": []
	},{
			"id": "problem_start_time",
			"order": 9,
			"controlType": "datetimepicker",
			"displayLabel": "Problem start time",
			"required": true
		}
	]
}
---
