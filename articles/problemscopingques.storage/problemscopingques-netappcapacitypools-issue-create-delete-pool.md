<properties
	articleId="issue-create-delete-pool"
	pageTitle="Issues creating or deleting a Capacity Pool"
	description="Issues creating or deleting a Capacity Pool"
	authors="b-tonya"
	ms.author="b-tonya"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32740754"
	productPesIds="16469"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureNetAppFiles"
/>
# Unable to move volume to destination Pool
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": true,
  "resourceRequired": true,
	"title": "Issues creating or deleting a Capacity Pool",
  	"fileAttachmentHint": "",
  	"formElements": [ {
  			"id": "problem_start_time",
      			"order": 1,
      			"controlType": "datetimepicker",
      			"displayLabel": "When did the problem start?",
      			"required": true
		}, {
            		"id": "netapp_account",
            		"order": 2,
            		"controlType": "dropdown",
            		"displayLabel": "NetApp Account",
            		"watermarkText": "Choose an option",
            		"dynamicDropdownOptions": {
                		"uri": "/subscriptions/{subscriptionid}/resourceGroups/{resourcegroup}/providers/Microsoft.NetApp/netAppAccounts?api-version=2019-11-01",
                		"jTokenPath": "value",
                		"textProperty": "id",
                		"valueProperty": "id",
                		"textPropertyRegex": "[^/]+$",
                		"defaultDropdownOptions": {
					"value": "dont_know_answer",
					"text": "None of the above"
                			}
				},
            		"dropdownOptions": [{
                    		"value": "NoNetAppAccount",
                    		"text": "Did not find the netapp account"
                		}
			],
            		"required": true
    		}, {
      			"id": "pool_name",
      			"order": 3,
      			"controlType": "textbox",
      			"displayLabel": "Capacity Pool Name",
      			"watermarkText": "Name of Capacity Pool used",
      			"required": false
    		}, {
      			"id": "problem_description",
      			"order": 4,
      			"controlType": "multilinetextbox",
      			"displayLabel": "Provide any additional details",
      			"required": true,
      			"useAsAdditionalDetails": true
    		}, {
      			"id": "error_message",
      			"order": 5,
     			"controlType": "textbox",
      			"displayLabel": "Error message",
      			"watermarkText": "What was the error message?",
      			"required": false
    		}
  	]
}
---
