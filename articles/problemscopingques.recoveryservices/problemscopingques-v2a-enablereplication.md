<properties
	pageTitle="V2A Enable Replication"
	description="V2A Enable Replication"
	authors="srinathv"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32536405"
	productPesIds="15207"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# V2A Enable Replication
---
{
	"resourceRequired": false,
	"title": "V2A Enable Replication",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "learn_more_text",
			"order": 1,
			"controlType": "infoblock",
			"content": "<b>Review the resources listed as they may help you solve your issue without needing to open a support case</b>  
				<ul><li>Ensure all the prerequisites mentioned in <a href='https://aka.ms/v2asupportmatrix'>Support Matrix</a> are met</li> <li>On-premises VMs that you replicate to Azure must meet the <a href='https://docs.microsoft.com/azure/site-recovery/support-matrix-vmware-to-azure#azure-vm-requirements'>Azure VM requirements</a></li></ul>"
		},  {
			"id": "problem_os_version",
			"order": 2,
			"controlType": "textbox",
			"displayLabel": "What is the Operating System version (and kernel version for Linux) of the VM that you are trying to protect?",
			"watermarkText": "Ex: Windows Server 2016, Ubuntu 16.04 LTS server kernel 4.10.0-14-generic to 4.10.0-32-generic",
			"useAsAdditionalDetails": false,
			"required": true
		}, {
			"id": "learn_more_text_1",
			"order": 3,
			"controlType": "infoblock",
			"content": "To find the list of supported Operating System <a href='https://docs.microsoft.com/azure/site-recovery/support-matrix-vmware-to-azure#replicated-machines'>visit here</a>."
		}, {
			"id": "problem_source_machine_name",
			"order": 4,
			"controlType": "textbox",
			"displayLabel": "What is the name of the VM that you are trying to protect?",
			"useAsAdditionalDetails": false,
			"required": false
		}, {
			"id": "learn_more_text_2",
			"order": 5,
			"controlType": "infoblock",
			"content": "<b>Review steps listed below for Enable Protection job, provide the STATUS and check the links below to find resolutions to common issues:</b>"
		}, {
			"id": "Prerequisites check for enable protection",
			"order": 6,
			"controlType": "dropdown",
			"displayLabel": "Step 1: Prerequisites check for enable protection",
			"watermarkText": "Choose the job STATUS",
			"dropdownOptions": [{
					"value": "This step was Successful",
					"text": "This step was Successful"
				}, {
					"value": "Failed",
					"text": "Failed"
				}
			],
			"required": true
		},  {
			"id": "learn_more_text_3",
			"order": 7,
			"controlType": "infoblock",
			"content": "Ensure all the prerequisites mentioned in <a href='https://aka.ms/v2asupportmatrix'>Support Matrix</a> are met."
		}, {
			"id": "Installing Mobility Services and preparing target",
			"order": 8,
			"controlType": "dropdown",
			"displayLabel": "Step 2: Installing Mobility Services and preparing target",
			"watermarkText": "Choose the job STATUS",
			"dropdownOptions": [{
					"value": "This step was Successful",
					"text": "This step was Successful"
				}, {
					"value": "Failed: Error 95105 - Protection could not be enabled (EP0856)",
					"text": "Failed: Error 95105 - Protection could not be enabled (EP0856)"
				}, {
					"value": "Failed: Error 95107 - Protection could not be enabled (EP0858)",
					"text": "Failed: Error 95107 - Protection could not be enabled (EP0858)"
				}, {
					"value": "Failed: Error 95117 - Protection could not be enabled (EP0865)",
					"text": "Failed: Error 95117 - Protection could not be enabled (EP0865)"
				}, {
					"value": "Failed: Error 95103 - Protection could not be enabled (EP0854)",
					"text": "Failed: Error 95103 - Protection could not be enabled (EP0854)"
				}, {
					"value": "Failed: Error 95213 - Protection could not be enabled (EP0874)",
					"text": "Failed: Error 95213 - Protection could not be enabled (EP0874)"
				}, {
					"value": "Failed: Error 95108 - Protection could not be enabled (EP0859)",
					"text": "Failed: Error 95108 - Protection could not be enabled (EP0859)"
				}, {
					"value": "Failed: Error 95265 - Protection could not be enabled (EP0902)",
					"text": "Failed: Error 95265 - Protection could not be enabled (EP0902)"
				}, {
					"value": "Failed: Error 95224 - Protection could not be enabled (EP0883)",
					"text": "Failed: Error 95224 - Protection could not be enabled (EP0883)"
				}, {
					"value": "my error code is not listed here",
					"text": "my error code is not listed here"
						}
					],
			"required": true
		},  {
			"id": "learn_more_text_4",
			"order": 9,
			"controlType": "infoblock",
			"content": "Find resolutions to error codes in <a href='https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-push-install-error-codes'>troubleshoot Mobility Service push installation issues</a> article."
		}, {		
			"id": "Enable replication",
			"order": 7,
			"controlType": "dropdown",
			"displayLabel": "Step 3: Enable replication",
			"watermarkText": "Choose the job STATUS",
			"dropdownOptions": [{
					"value": "Successful",
					"text": "Successful"
				}, {
					"value": "Failed",
					"text": "Failed"
				}
			],
			"required": true
		},  {
			"id": "learn_more_text_5",
			"order": 10,
			"controlType": "infoblock",
			"content": "Ensure all the prerequisites mentioned in <a href='https://aka.ms/v2asupportmatrix'>Support Matrix</a> are met."
		}, {
			"id": "Starting initial replication",
			"order": 7,
			"controlType": "dropdown",
			"displayLabel": "Step 4: Starting initial replication",
			"watermarkText": "Choose the job STATUS",
			"dropdownOptions": [{
					"value": "This step was Successful",
					"text": "This step was Successful"
					}, {
						"value": "Initial replication stuck at 0%",
						"text": "Initial replication stuck at 0%"
					}, {
						"value": "Initial replication stuck at >0%",
						"text": "Initial replication stuck at >0%"
				}, {
					"value": "Failed",
					"text": "Failed"
				}
			],
			"required": true
		},  {
				"id": "learn_more_text_6",
				"order": 11,
				"controlType": "infoblock",
				"content": "Follow steps listed in this<a href='https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-protection-troubleshoot'>article</a> to resolve common issue."
		},  {
			"id": "I have other issues",
			"order": 12,
			"controlType": "dropdown",
			"displayLabel": "I have other issues",
			"watermarkText": "Choose the job STATUS",
			"dropdownOptions": [{
					"value": "Unable to find my source VM (or) its grayed out",
					"text": "Unable to find my source VM (or) its grayed out"
					}, {
					"value": "I tried to upgrade the ASR agents and it failed",
					"text": "I tried to upgrade the ASR agents and it failed"		
					}, {
					"value": "My VM is protected, but the health is in critical status",
					"text": "My VM is protected, but the health is in critical status"			
					}, {
					"value": "My VM is protected, but the application/crash consistent snapshot do not show the latest timestamp",
					"text": "My VM is protected, but the application/crash consistent snapshot do not show the latest timestamp"				
					}, {
					"value": "My issue is not listed here",
					"text": "My issue is not listed here"
				}
			],
			"required": true
		}, {
			"id": "problem_details",
			"order": 13,
			"controlType": "multilinetextbox",
			"displayLabel": "Please provide additional details:",
			"watermarkText": "Paste error message(s), error code(s) and describe the scenario(s) that are failing.",
			"required": true,
			"useAsAdditionalDetails": false
		}
]}
---
