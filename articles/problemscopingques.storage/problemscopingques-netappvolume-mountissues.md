<properties
	articleId="volume-mount-issues"
	pageTitle="Volume mount issues"
	description="Volume mount issues"
	authors="b-tonya"
	ms.author="b-tonya"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32740764"
	productPesIds="16469"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureNetAppFiles"
/>
# Volume mount issues
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": true,
  "resourceRequired": true,
	"title": "Volume mount issues",
  	"fileAttachmentHint": "",
  	"formElements": [ {
  			"id": "problem_start_time",
      			"order": 1,
      			"controlType": "datetimepicker",
      			"displayLabel": "When did the problem start?",
      			"required": true
		}, {
      			"id": "VolumeType",
      			"order": 2,
			"controlType": "dropdown",
            		"displayLabel": "What is the volume type?",
            		"watermarkText": "(i.e. SMB, Dual Protocol, NFSv3, NFSv4.1, NFSv4.1 Kerberos)",
			"dropdownOptions": [{
                   				"value": "SMB",
                    				"text": "SMB"
              				}, {
                    				"value": "Dual Protocol",
                    				"text": "Dual Protocol"
                			}, {
                    				"value": "NFSv3",
                    				"text": "NFSv3"
                            }, {
                    				"value": "NFSv4.1",
                    				"text": "NFSv4.1 "
                			}, {
                    				"value": "NFSv4.1 Kerberos",
                    				"text": "NFSv4.1 Kerberos"
                			}, {
                    				"value": "dont_know_answer",
                    				"text": "None of the above"
                			}
			],
            		"required": true
		}, {
			"id": "DNSreachable",
			"order": 3,
			"controlType": "dropdown",
			"displayLabel": "Is your DNS server IP addresses reachable?",
			"watermarkText": "If there’s no issues with the DNS server IP addresses, then verify that no firewalls are blocking the access?",
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
      			"id": "operating_system",
      			"order": 4,
      			"controlType": "multilinetextbox",
      			"displayLabel": "Provide any details on the operating system where the mount is being performed?",
      			"required": false,
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
      			"watermarkText": "What was the error message?",
      			"required": false
    		}
  	]
}
---
