<properties
	articleId="issue-create-delete-netapp-account"
	pageTitle="Issues creating or deleting a NetApp Account"
	description="Issues creating or deleting a NetApp Account"
	authors="b-tonya"
	ms.author="b-tonya"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32640625"
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
	"title": "Issues creating or deleting a NetApp Account",
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
            		"watermarkText": "Select NetApp Account",
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
      			"id": "netapp_account_name",
      			"order": 3,
      			"controlType": "textbox",
						"visibility": "netapp_account != null && netapp_account == NoNetAppAccount"
      			"displayLabel": "NetApp Account Name",
      			"watermarkText": "Name of NetApp Account used",
      			"required": false
    		}, {
      			"id": "resource_group_name",
      			"order": 4,
      			"controlType": "textbox",
      			"displayLabel": "Resource Groups Name",
      			"watermarkText": "Name of Resource Group used",
      			"required": false
    		}, {
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
