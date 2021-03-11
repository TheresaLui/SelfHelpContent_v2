<properties
	articleId="Performance Issues"
	pageTitle="Performance Issues"
	description="Performance issues with volume throughput or latency"
	authors="b-tonya"
	ms.author="b-tonya"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32640632,32640631"
	productPesIds="16469"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureNetAppFiles"
/>
# Performance issues with volume throughput or latency
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": true,
  "resourceRequired": false,
	"title": "Performance issues with volume throughput or latency",
  	"fileAttachmentHint": "",
  	"formElements": [ {
  					"id": "problem_start_time",
      			"order": 1,
      			"controlType": "datetimepicker",
      			"displayLabel": "When did the problem start?",
      			"required": true
				}, {
      			"id": "vm_os_type",
      			"order": 2,
      			"controlType": "textbox",
      			"displayLabel": "Provide details on the virtual machine and operating system(s) that is experiencing performance issue?",
						"watermarkText": "",
      			"required": false
    		}, {
		      	"id": "volume_vm_same_region",
		      	"order": 3,
						"controlType": "dropdown",
		        "displayLabel": "Are the volume(s) and virtual machine(s) in the same region?",
		        "watermarkText": "",
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
		      	"id": "accelerated_networking",
		      	"order": 4,
						"controlType": "dropdown",
		        "displayLabel": "Is Accelerated Networking enabled on the network interface of the virtual machine(s)?",
		        "watermarkText": "",
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
      			"id": "ping_mount_ip",
      			"order": 5,
      			"controlType": "textbox",
      			"displayLabel": "When experience performance issue, are you able to ping the mount ip address?",
      			"watermarkText": "",
      			"required": false
    		}, {
      			"id": "protocol_settings",
      			"order": 6,
      			"controlType": "textbox",
      			"displayLabel": "Which of the protocol specific settings are enabled?",
      			"watermarkText": "i.e. SMB Signing, SMB Encryption, NFSv4.1 Kerberos, etc",
      			"required": false
    		}, {
      			"id": "problem_description",
      			"order": 7,
      			"controlType": "multilinetextbox",
      			"displayLabel": "Provide any additional details",
      			"required": true,
      			"useAsAdditionalDetails": true
    		}
  	]
}
---
