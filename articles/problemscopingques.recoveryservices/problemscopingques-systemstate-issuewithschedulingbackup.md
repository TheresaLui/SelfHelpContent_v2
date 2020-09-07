<properties
         pageTitle="Scoping questions for Configuration - issues with scheduling backup"
         description="Scoping questions for Configuration - issues with scheduling backup"
         authors="srinathvasireddy"
         ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32594868"
         productPesIds="15207"
         cloudEnvironments="public, fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="bdb1bfbf-d4fc-4dba-aca7-33cecf8e881f"
	ownershipId="StorageMediaEdge_Backup"
/>
# Questions for Configuration - issues with scheduling backup
---

{
         "resourceRequired": false,
         "subscriptionRequired": false,
         "title": "Issue with scheduling backup",
         "fileAttachmentHint": "",
	 "diagnosticCard": {
		"title": "Issue with scheduling backup",
		"description": "These diagnostics will check for errors.",
		"insightNotAvailableText": "We didn't find any problems"
	    },
         "formElements": [{
		          "id": "issue_type",
                          "order": 1,
                          "controlType": "dropdown",
		          "displayLabel": "Which type of issue you are facing?",
                          "watermarkText": "Select",
		          "dropdownOptions":[{
                                      "value": "Unable to add items",
                                      "text": "Unable to add items"
                                    },{
                                      "value": "Unable to see files/Folders while scheduling backup",
                                      "text": "Unable to see files/Folders while scheduling backup"
                                    },{
                                      "value": "Unable to modify backup schedule",
                                      "text": "Unable to modify backup schedule"
                                    },{
                                      "value": "Unable to modify retention policy",
                                      "text": "Unable to modify retention policy"
                                    },{
                                      "value": "Unable to select files/folders for backup",
                                      "text": "Unable to select files/folders for backup"
                                    },{
                                      "value": "Agent console hangs",
                                      "text": "Agent console hangs"
                                    },{
                                      "value": "dont_know_answer",
                                      "text": "Other, don't know or not applicable"
                                    }
                              ],
		      "required": true,
     "diagnosticInputRequiredClients": "Portal"
	  },{
                          "id": "problem_start_time",
                          "order": 2,
                          "visibility": "null",
                          "controlType": "datetimepicker",
                          "displayLabel": "When did the problem begin?",
                          "required": true,
     "diagnosticInputRequiredClients": "Portal"
             },{
                          "id": "problem_description",
                          "order": 3,
                          "controlType": "multilinetextbox",
                          "useAsAdditionalDetails": true,
                          "displayLabel": "Additional details",
                          "watermarkText": "Provide additional information about your issue",
                          "required": true,
                          "hints": []
		}
		],
"$schema": "SelfHelpContent"
}
---
