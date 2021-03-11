<properties
	articleId="NetAppVolumeLatencyIssues"
	description="Issues with volume latency"
	pageTitle="Issues with volume latency"
	authors="b-tonya"
	ms.author="b-tonya"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32640632"
	productPesIds="16469"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureNetAppFiles"
/>
# Volume latency is higher than expected
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": true,
  "resourceRequired": true,
	"title": "Volume latency is higher than expected",
  	"fileAttachmentHint": "",
  	"formElements": [ {
  			"id": "problem_start_time",
      			"order": 1,
      			"controlType": "datetimepicker",
      			"displayLabel": "When did the problem start?",
      			"required": true
		}, {
		        "id": "ping_volume",
            		"order": 2,
            		"ControlType": "dropdown",
            		"displayLabel": "Are you able to ping the mount IP address for the volume that is experiencing performance issues?",
			"dropdownOptions": [
					{
                    				"value": "Yes",
                    				"text": "Yes"
                			},
                			{
                    				"value": "No",
                    				"text": "No"
                			},
					{
                    				"value": "dont_know_answer",
                    				"text": "None of the above"
                			}
			],
            			"required": true
		}, {
		        "id": "accelerated_networking",
            		"order": 3,
            		"ControlType": "dropdown",
            		"displayLabel": "Is Accelerated Networking enabled?",
			"dropdownOptions": [
					{
                    				"value": "Yes",
                    				"text": "Yes"
                			},
                			{
                    				"value": "No",
                    				"text": "No"
                			},
					{
                    				"value": "dont_know_answer",
                    				"text": "None of the above"
                			}
			],
            			"required": true
		}, {
				"id": "volume_vm_same_region",
				"order": 4,
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
      			"id": "client_workload_operating_system",
      			"order": 5,
      			"controlType": "textbox",
      			"displayLabel": "Provide  details on what workload and operating system mounted to the volume?",
      			"required": false
    		}, {
      			"id": "How many clients are accessing the volume?",
      			"order": 6,
      			"controlType": "textbox",
      			"displayLabel": "How many clients are accessing the volume?",
      			"required": false
    		}, {
      			"id": "protocol_settings",
      			"order": 7,
      			"controlType": "textbox",
      			"displayLabel": "Which of the protocol specific settings are enabled?",
      			"watermarkText": "i.e. SMB Signing, SMB Encryption, NFSv4.1 Kerberos, etc",
      			"required": false
    		}, {
      			"id": "problem_description",
      			"order": 8,
      			"controlType": "multilinetextbox",
      			"displayLabel": "Provide any additional details",
      			"required": true,
      			"useAsAdditionalDetails": true
    		}
  	]
}
---
