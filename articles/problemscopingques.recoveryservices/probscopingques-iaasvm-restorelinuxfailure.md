<properties
         pageTitle="Scoping questions for Azure VM Restore failure for Linux"
         description="Scoping questions for Azure VM Restore failure for Linux"
         authors="srinathvasireddy"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32553297"
         productPesIds="15207"
         cloudEnvironments="public"
         schemaVersion="1"
/>
# Questions Azure VM Restore failure for Linux 
---
{
         "resourceRequired": true,
         "title": "Azure VM Restore failure for Linux",
         "fileAttachmentHint": "",
         "formElements": [{
			  "id": "using_VM",
                          "order": 1,
                          "controlType": "textbox",
			  "displayLabel": "Which virtual machine(s) is experiencing the problem?",
                          "watermarkText": "Enter the name of the virtual machine(s)",
             	          "required": true
		   },{
                          "id": "JobID_Name",
                          "order": 2,
                          "controlType": "textbox",
			  "displayLabel": "Enter the failed restore job activity ID:",
                    	  "watermarkText": "Ex. cace7461-dd3c-4e38-b4db-38dc57fdee7b",
                          "required": true
	   	},{
                          "id": "learn_more_text",
                          "order": 3,
                          "controlType": "infoblock",
                          "content": " Microsoft can provide a solution to your problem faster if you can provide a failed Backup Job Activity ID. From a new browser tab, You can find this from Recovery Services Vault > Monitoring and Report > Backup Jobs > Failed > Activity ID."
                },{
			  "id": "Restoration_Type",
                          "order": 4,
                          "controlType": "dropdown",
         	 	  "displayLabel": "Which type of restore are you performing?",
                          "watermarkText": "Select",
                          "dropdownOptions": [{
                                        "value": "Restoring VMs in Azure Portal",
     					"text": "Restoring VMs in Azure Portal"
				},{
					"value": "Recovering files from Azure VMs backups",
					"text": "Recovering files from Azure VMs backups"
				},{
					"value": "Restore encrypted VMs",
					"text": "Restore encrypted VMs"
				}
			],
				"required": true
			}
		]
	}
---
