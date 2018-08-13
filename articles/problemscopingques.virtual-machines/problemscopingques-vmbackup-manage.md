<properties
         pageTitle="Scoping questions for Azure VM backup management issues"
         description="Scoping questions for Azure VM backup management issues"
         authors="srinathvasireddy"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32565495"
         productPesIds="14749"
         cloudEnvironments="public"
         schemaVersion="1"
/>
# Questions Azure VM backup management
---
{
         "resourceRequired": true,
         "title": "Azure VM backup or restore failure",
         "fileAttachmentHint": "",
         "formElements": [{
		          "id": "vm_facing_issue",
                          "order": 1,
                          "controlType": "textbox",
                 	  "displayLabel": "Which virtual machine(s) is experiencing problem?",
                          "watermarkText": "Enter the name of the virtual machine(s)",
        	         	  "required": true
						},{
						  "id": "issue_Type",
                          "order": 2,
                          "controlType": "dropdown",
                 	  	  "displayLabel": "Which type of issue you are facing?",
                          "watermarkText": "Choose an option",
			"dropdownOptions":[{
				"value": "Backup failure",
				"text": "Backup failure"
			 },{
			        "value": "Restore failure",
				"text": "Restore failure"
			   }
			   ],
			   "required": true
			 },{
			  "id": "backup_JobID_Name",
                          "order": 3,
			  "visibility": "issue_Type == Backup failure",
                          "controlType": "textbox",
                          "displayLabel": "Enter the failed backup job Activity ID:",
                          "watermarkText": "Ex. cace7461-dd3c-4e38-b4db-38dc57fdee7b",
                          "required": true
						},{
						  "id": "restore_JobID_Name",
                          "order": 4,
						  "visibility": "issue_Type == Restore failure",
                          "controlType": "textbox",
                  		  "displayLabel": "Enter the failed restore job Activity ID:",
                          "watermarkText": "Ex. cace7461-dd3c-4e38-b4db-38dc57fdee7b",
                          "required": true
						},{
						  "id": "learn_more_text",
                          "order": 5,
						  "visibility": "issue_Type == Restore failure || issue_Type == Backup failure",
                          "controlType": "infoblock",
                          "content": "Microsoft can provide a solution to your problem faster if you can provide failed Job Activity ID. From a new browser tab, You can find this from Recovery Services Vault > Monitoring and Report > Backup Jobs > In progress > Activity ID"
						},{
			 			 "id": "select_ErrorMessage_Backup",
                          "order": 6,
						  "visibility": "issue_Type == Backup failure",
                          "controlType": "dropdown",
                  	  	  "displayLabel": "Select the error message that you are seeing?",
                          "watermarkText": "Select",
                          "droupdownOptions": [
							{
							  "value": "VM Agent is unable to communicate with azure backup service",
							  "text": "VM Agent is unable to communicate with Azure Backup service"
							},{
							   "value": "Could not communicate with the VM agent for snapshot status",
							   "text": "Could not communicate with the VM agent for snapshot status"
							},{
							   "value": "Snapshot operation failed due to no network connectivity on the virtual machine",
							   "text": " Snapshot operation failed due to no network connectivity on the virtual machine"
							},{
								"value": "Could not copy the snapshot of the virtual machine...",
								"text": "Could not copy the snapshot of the virtual machine..."
							},{
								"value": "Could not communicate with the VM agent for snapshot status",
								"text": "Could not communicate with the VM agent for snapshot status"
							},{
								"value": "VM is in Failed Provisioning State",
								"text": "VM is in Failed Provisioning State"
							},{
								"value": "Currently Azure Backup does not support disk sizes greater than 1023GB",
								"text": "Currently Azure Backup does not support disk sizes greater than 1023GB"
							},{
								"value": "My error message is not listed here",
								"text": "My error message is not listed here"
							  }
						],
			 					"required": true
						},{
							"id": "basic_troubleshooting_multiselect",
							"order": 7,
							"visibility": "issue_Type == Backup failure",
							"controlType": "multiselectdropdown",
							"displayLabel": "Select the troubleshooting steps you have completed:",
							"dropdownOptions": [{
                                     					"value": "VM Agent (WA Agent) has latest version",
                                     					"text": "VM Agent (WA Agent) has latest version"
                                   				  },{
														"value": "​VM OS version is supported",
                                     					"text": "​VM OS version is supported"
                                   				  },{
														"value": "VM has internet connectivity",
														"text": "VM has internet connectivity"
                                   				  },{
                                            			"value": "Vault is upgraded to new vault stack V2",
                                            			"text": "Vault is upgraded to new vault stack V2"
                                   				  },{
														"value": "Another backup service is not running",
														"text": "Another backup service is not running"
													},
        					                  ],
                   					"required": true
						},{
						  "id": "restoration_Type",
						  "visibility": "issue_Type == Restore failure",
                          "order": 8,
                          "controlType": "dropdown",
         	 	 		  "displayLabel": "Which type of restore you are performing?",
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
				]}
---
