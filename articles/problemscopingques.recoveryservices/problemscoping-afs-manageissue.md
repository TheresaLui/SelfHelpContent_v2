<properties
         pageTitle="Scoping questions for Azure File Share backup management issue"
         description="Scoping questions for Azure File Share backup management issue"
         authors="srinathvasireddy"
		     ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32612213"
         productPesIds="15207"
         cloudEnvironments="public"
         schemaVersion="1"
		     articleId="04e81c26-e724-4026-b744-0edbf9ae5eeb"
/>
# Questions for Azure File Share backup management issue
---
{
         "resourceRequired": true,
		     "subscriptionRequired": true,
         "title": "Azure File share backup management issue",
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
							"displayLabel": "Provide the name(s) of the File Share which is facing management issue",
							"watermarkText": "Enter file share name(s) comma separated",
							"required": false
					},{
							"id": "management_issue_type",
							"order": 3,
							"controlType": "multiselectdropdown",
							"infoBalloonText": "Check <a href='https://aka.ms/AB-AFS-ManageAFS'>manage Azure File Share backups</a> article",
							"displayLabel": "Which type of management issue you are facing?",
							"dropdownOptions": [{
												"value": "Monitor jobs",
												"text": "Monitor jobs"
										},{
												"value": "Create a new policy",
												"text": "Create a new policy"
										},{
												"value": "Stop protection on a file share",
												"text": "Stop protection on a file share"
										},{
												"value": "Resume protection on a file share",
												"text": "Resume protection on a file share"
										},{
												"value": "Delete backup data",
												"text": "Delete backup data"
										},{
												"value": "dont_know_answer",
												"text": "Other, don't know or not applicable"
										}
									 ],
										"required": true
					},{
							"id": "error_code",
							"order": 5,
							"controlType": "textbox",
							"displayLabel": "Provide the error code if you are seeing",
							"watermarkText": "Example: DataTransferServiceCoFLimitReached",
							"required": false
					},{
						  "id": "problem_start_time",
						  "order": 6,
						  "controlType": "datetimepicker",
						  "displayLabel": "When did the problem begin?",
						  "required": true
					},{
						  "id": "problem_description",
						  "order": 7,
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
