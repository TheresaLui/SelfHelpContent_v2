<properties
	articleId="issue-create-delete-smb-volume"
	pageTitle="Issues creating or deleting a SMB Volume"
	description="Issues creating or deleting a SMB Volume"
	authors="b-tonya"
	ms.author="b-tonya"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32740756"
	productPesIds="16469"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureNetAppFiles"
/>
# Issues creating or deleting a SMB Volume
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": true,
  "resourceRequired": true,
	"title": "Issues creating or deleting a SMB Volume",
  	"fileAttachmentHint": "",
  	"formElements": [ {
  			"id": "problem_start_time",
      			"order": 1,
      			"controlType": "datetimepicker",
      			"displayLabel": "When did the problem start?",
      			"required": true
		}, {
      			"id": "AADDS",
      			"order": 2,
			"controlType": "dropdown",
            		"displayLabel": "Is Azure ADDS used?",
            		"watermarkText": "Is Azure ADDS used?",
			"dropdownOptions": [{
                   				"value": "Yes",
                    				"text": "Yes"
              				}, {
                    				"value": "No",
                    				"text": "No"
                			}, {
                    				"value": "dont_know_answer",
                    				"text": "None of the above"
                			}
			],
            		"required": true
		}, {
			"id": "reverselookup",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "Is PTR of AD machine added in DNS?",
			"watermarkText": "Is PTR of AD machine added in DNS?",
			"dropdownOptions": [{
						"value": "Yes",
						"text": "Yes"
					}, {
						"value": "No",
						"text": "No"
					}, {
						"value": "dont_know_answer",
						"text": "None of the above"
					}
			],
			"required": false
    		}, {
      			"id": "volume_size",
      			"order": 4,
      			"controlType": "multilinetextbox",
      			"displayLabel": "Volume size (GiB)",
      			"required": true,
      			"useAsAdditionalDetails": false
    		},  {
      			"id": "problem_description",
      			"order": 5,
      			"controlType": "multilinetextbox",
      			"displayLabel": "Provide any additional details",
      			"required": true,
      			"useAsAdditionalDetails": true
    		}, {
      			"id": "error_message",
      			"order": 6,
     			  "controlType": "textbox",
      			"displayLabel": "Error message",
      			"watermarkText": "What was the error message",
      			"required": false
    		}
  	]
}
---
