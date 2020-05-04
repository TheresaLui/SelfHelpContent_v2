<properties
         pageTitle="Scoping questions for IAAS VM howto and general quest"
         description="Scoping questions for IAAS VM howto and general quest"
         authors="srinathvasireddy"
	 ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32637323,32637324,32637325"
         productPesIds="14749,15571,15797,16454,16470"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
	 articleId="decf02f8-2db8-4b8f-a24d-00bdd0ca9195"
	ownershipId="StorageMediaEdge_Backup"
/>
# Questions for IAAS VM howto and general quest
---
{
         "resourceRequired": false,
	       "subscriptionRequired": false,
         "title": "IAAS VM how-to and general questions",
         "fileAttachmentHint": "",
         "formElements": [{
	       "id": "operation_type",
	       "visibility": "null",
              "order": 1,
              "controlType": "dropdown",
              "displayLabel": "Choose the topic that you have question about:",
              "watermarkText": "Select",
	      "dropdownOptions":[{
							"value": "Backup",
							"text": "Backup"
						},{
							"value": "Restore",
							"text": "Restore"
						},{
							"value": "Policy",
							"text": "Policy"
						},{
							"value": "Snapshots/Recovery Points",
							"text": "Snapshots/Recovery Points"
						},{
							"value": "Limitations/Pre-requisites/(Not) Supported scenarios",
							"text": "Limitations/Pre-requisites/(Not) Supported scenarios"
						},{
							"value": "Performance",
							"text": "Performance"
						},{
							"value": "Best Practices",
							"text": "Best Practices"
						},{
							"value": "Pricing",
							"text": "Pricing"
						},{
							"value": "Security",
							"text": "Security"
						},{
							"value": "dont_know_answer",
							"text": "Other, don't know or not applicable"
						}
					],
					 "required": true
	},{
	      "id": "backup_dropdown",
              "order": 2,
              "visibility": "operation_type == Backup",
              "controlType": "dropdown",
               "infoBalloonText": "Check <a href='https://aka.ms/AB-AA4ecq2'>Configure backup</a>, <a href='https://aka.ms/AB-AzureVM-OnDemandBackup'>On-demand backup</a>, <a href='https://aka.ms/AB-AA4e56t'>Backup of encrypted VM</a>, <a href='https://aka.ms/AB-AA4ecql'>Manage Azure VM backup</a>, <a href='https://aka.ms/AB-AA4e56n'> Azure VM backup FAQs</a>",
              "displayLabel": "Choose an option that best describes your situation:",
              "watermarkText": "Select",
              "dropdownOptions": [{
                          "value": "How do I configure a scheduled backup?",
                          "text": "How do I configure a scheduled backup?"
		},{
			"value": "How do I take an on-demand backup?",
			"text": "How do I take an on-demand backup?"
		},{
			"value": "How do I take backup of encrypted VM?",
			"text": "How do I take backup of encrypted VM?"
		},{
			"value": "I have question about managed disks VM backup",
			"text": "I have question about managed disks VM backup"
		},{
			"value": "I have question about backup when VM is shut down",
			"text": "I have question about backup when VM is shut down"
		},{
			"value": "How do I stop protection while retaining my backed up data?",
			"text": "How do I stop protection while retaining my backed up data?"
		},{
			"value": "How do I stop protection and delete my backed up data?",
			"text": "How do I stop protection and delete my backed up data?"
		},{
			"value": "Why can't I see my VM in the Configure Backup wizard?",
			"text": "Why can't I see my VM in the Configure Backup wizard?"
		},{
			"value": "dont_know_answer",
			"text": "Other, don't know or not applicable"
		}
	],
  "required": false
          },{
                "id": "restore_dropdown",
		"order": 3,
		"visibility": "operation_type == Restore",
		"controlType": "dropdown",
		"infoBalloonText": "Check <a href='https://aka.ms/AB-Restore-FAQ'>Restore FAQs</a>",
		"displayLabel": "Choose an option that best describes your situation:",
		"watermarkText": "Select",
		"dropdownOptions": [{
				  "value": "How do I decide between Restore Disks vs. Full VM restore?",
				  "text": "How do I decide between Restore Disks vs. Full VM restore?"
			},{
				"value": "How do I restore managed disk VM?",
				"text": "How do I restore managed disk VM?"
			},{
				"value": "How do I restore VM to availability sets?",
				"text": "How do I restore VM to availability sets?"
			},{
				"value": "How do I restore a VM to a restore point before the VM was migrated to managed disks?",
				"text": "How do I restore a VM to a restore point before the VM was migrated to managed disks?"
			},{
				"value": "dont_know_answer",
				"text": "Other, don't know or not applicable"
			}
		],
		  "required": false
         },{
		"id": "policy_dropdown",
		"order": 4,
		"visibility": "operation_type == Policy",
		"controlType": "dropdown",
		"infoBalloonText": "Check <a href='https://aka.ms/AB-FAQ-InstantRestore'>Manage VM backups FAQ</a>",
		"displayLabel": "Choose an option that best describes your situation:",
		"watermarkText": "Select",
		"dropdownOptions": [{
					"value": "I have questions related to policy limit",
					"text": "I have questions related to policy limit"
				},{
					"value": "I have questions related to policy modification",
					"text": "I have questions related to policy modification"
				},{
					"value": "dont_know_answer",
					"text": "Other, don't know or not applicable"
				}
			],
			  "required": false
	},{
		"id": "Snapshots/Recovery Points",
		"order": 5,
		"visibility": "operation_type == Snapshots/Recovery Points",
		"controlType": "dropdown",
		"infoBalloonText": "Check <a href='https://aka.ms/AB-FAQ-InstantRestore'>Instant Restore FAQ</a>",
		"displayLabel": "Choose an option that best describes your situation:",
		"watermarkText": "Select",
"dropdownOptions": [{
			"value": "I have questions related to Snapshot",
			  "text": "I have questions related to Snapshot"
		},{
			"value": "I have questions related to Recovery Points",
			"text": "I have questions related to Recovery Points"
		},{
			"value": "dont_know_answer",
			"text": "Other, don't know or not applicable"
		}
	],
"required": false
	 },{
		"id": "Limitations/Pre-requisites/(Not) Supported scenarios",
		"order": 6,
		"visibility": "operation_type == Limitations/Pre-requisites/(Not) Supported scenarios",
		"controlType": "dropdown",
		"infoBalloonText": "Check <a href='https://aka.ms/AA4evhu'>Pre-requisites</a>, <a href='https://aka.ms/AB-AA4ecqa'>Support Matrix</a> for Azure VM backup",
		"displayLabel": "Choose an option that best describes your situation:",
		"watermarkText": "Select",
		"dropdownOptions": [{
			"value": "What Azure VMs can I back up using Azure Backup?",
			"text": "What Azure VMs can I back up using Azure Backup?"
		},{
			"value": "I have questions about Azure VM Backup supported scenarios",
			"text": "I have questions about Azure VM Backup supported scenarios"
		},{
			  "value": "I have questions about Azure VM Backup unsupported scenarios",
			"text": "I have questions about Azure VM Backup unsupported scenarios"
		},{
			"value": "I have questions about Azure VM Backup limitations ",
			"text": "I have questions about Azure VM Backup limitations "
		},{
			  "value": "I have questions about Azure VM Backup pre-requisites",
			"text": "I have questions about Azure VM Backup pre-requisites"
		},{
			"value": "dont_know_answer",
			"text": "Other, don't know or not applicable"
		}
	],
		"required": false
	 },{
		"id": "Backup/Restore_performance",
		"order": 7,
		"visibility": "operation_type == Performance",
		"controlType": "dropdown",
		"infoBalloonText": "Check <a href='https://aka.ms/AB-Restore-FAQ'>Restore FAQs</a>, <a href='https://aka.ms/AB-BackupRestoreConsid'>Backup and Restore consideration</a>, <a href='https://aka.ms/AB-AA4ecqb'>Backup performance</a>",
		"displayLabel": "Choose an option that best describes your situation:",
		"watermarkText": "Select",
		"dropdownOptions": [{
					"value": "I have questions about restore performance",
					"text": "I have questions about restore performance"
				},{
					"value": "I have questions about backup performance",
					"text": "I have questions about backup performance"
				},{
					"value": "dont_know_answer",
					"text": "Other, don't know or not applicable"
				}
			],
	  "required": false
	},{
		"id": "Best_Practices",
		"order": 8,
		"visibility": "operation_type == Best Practices",
		"controlType": "dropdown",
		"infoBalloonText": "Check <a href='https://aka.ms/AB-AA4e56d'>Best Practices</a> for Azure VM backup",
		"displayLabel": "Choose an option that best describes your situation:",
		"watermarkText": "Select",
		"dropdownOptions": [{
					"value": "I have questions about VM backup best practices",
					"text": "I have questions about VM backup best practices"
				},{
					"value": "dont_know_answer",
					"text": "Other, don't know or not applicable"
				}
			],
		  "required": false
		},{
		"id": "Pricing",
		"order": 9,
		"visibility": "operation_type == Pricing",
		"controlType": "dropdown",
		"infoBalloonText": "Check <a href='https://aka.ms/AB-Costs'>Azure backup costs</a> article",
		"displayLabel": "Choose an option that best describes your situation:",
		"watermarkText": "Select",
		"dropdownOptions": [{
					"value": "I have questions about backup cost",
					"text": "I have questions about backup cost"
				},{
					"value": "dont_know_answer",
					"text": "Other, don't know or not applicable"
				}
			],
		"required": false
	},{
		"id": "Security",
		"order": 10,
		"visibility": "operation_type == Security",
		"controlType": "dropdown",
		"infoBalloonText": "Check <a href='https://aka.ms/AB-AA4e56n'>Backup FAQs</a>, <a href='https://aka.ms/AB-Restore-Permissions'>Restore permissions</a> article",
		"displayLabel": "Choose an option that best describes your situation:",
		"watermarkText": "Select",
		"dropdownOptions": [{
					"value": "What permissions are required to enable VM backup?",
					"text": "What permissions are required to enable VM backup?"
				},{
					"value": "What permissions are required for restore operation?",
					"text": "What permissions are required for restore operation?"
				},{
					"value": "dont_know_answer",
					"text": "Other, don't know or not applicable"
				}
			],
			  "required": false
	},{
		"id": "problem_start_time",
		"order": 11,
		"visibility": "null",
		"controlType": "datetimepicker",
		"displayLabel": "When did the problem begin?",
		"required": true
           },{
		  "id": "problem_description",
		  "order": 12,
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
