<properties
	articleId="unable-to-resize-volume"
	pageTitle="Unable to resize volume"
	description="Unable to resize volume"
	authors="b-tonya"
	ms.author="b-tonya"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32740777"
	productPesIds="16469"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureNetAppFiles"
/>
# Unable to resize volume
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": true,
  "resourceRequired": true,
	"title": "Unable to resize volume",
  	"fileAttachmentHint": "",
  	"formElements": [ {
  			"id": "problem_start_time",
      			"order": 1,
      			"controlType": "datetimepicker",
      			"displayLabel": "When did the problem start?",
      			"required": true
		}, {
      			"id": "new_volume_size",
      			"order": 2,
      			"controlType": "multilinetextbox",
      			"displayLabel": "What is the new size of the volume (GiB)",
      			"required": true,
      			"useAsAdditionalDetails": false
    		},  {
      			"id": "problem_description",
      			"order": 3,
      			"controlType": "multilinetextbox",
      			"displayLabel": "Provide any additional details",
      			"required": true,
      			"useAsAdditionalDetails": true
    		}, {
      			"id": "error_message",
      			"order": 4,
     			  "controlType": "textbox",
      			"displayLabel": "Error message",
      			"watermarkText": "What was the error message?",
      			"required": false
    		}
  	]
}
---
