<properties
         pageTitle="Scoping questions for MARS Issue with scheduling backup"
         description="ScScoping questions for MARS Issue with scheduling backup"
         authors="srinathvasireddy"
	 ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32632795"
         productPesIds="15207"
         cloudEnvironments="public, fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="3ea09efb-a567-489d-b188-71b42a03bd64"
	ownershipId="StorageMediaEdge_Backup"
/>
# Questions for MARS Issue with scheduling backup
---
{
         "resourceRequired": false,
         "subscriptionRequired": false,
         "title": "Issue with scheduling backup",
         "fileAttachmentHint": "",
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
			 "required": true
	    },{
                          "id": "problem_start_time",
                          "order": 2,
                          "visibility": "null",
                          "controlType": "datetimepicker",
                          "displayLabel": "When did the problem begin?",
                          "required": true
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
