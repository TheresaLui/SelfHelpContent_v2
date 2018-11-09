<properties
         pageTitle="Scoping questions for Vmware to Azure enable replication"
         description="Scoping questions for Vmware to Azure enable replication"
         authors="Rajeswari-mamilla"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32536405"
         productPesIds="16370"
         cloudEnvironments="public"
         schemaVersion="1"
/>
# Questions Azure site recovery - Vmware to Azure Enable replication
---
{
         "resourceRequired": true,
         "title": "Site recovery enable replication failure",
         "fileAttachmentHint": "",
         "formElements": [{
                          "id": "os_version",
                          "order": 1,
			      "visibility": "null",
                          "controlType": "textbox",
                          "displayLabel": "What is the OS version of the impacted Server?",
                          "watermarkText": ""Ex: Windows Server 2016, Ubuntu 16.04 LTS server kernel 4.10.0-14-generic to 4.10.0-32-generic",
                          "required": true
                        }, {
			                "id": "learn_more_text_1",
			                "order": 2,
                    "visibility": "null",
			                "controlType": "infoblock",
			                "content": "To find the list of supported Operating System <a href='https://docs.microsoft.com/azure/site-recovery/support-matrix-vmware-to-azure#replicated-machines'>visit here</a>."
		                }, {
                        
                           "id": "problem_source_machine_name",
			                "order": 3,
                    "visibility": "null",
			                "controlType": "textbox",
			                "displayLabel": "Provide the host name of the VM (or) failed Job Id:",
			                "watermarkText": "Get failed Job Id from (Using new browser tab): Recovery Services Vault > Jobs > Site Recovery Jobs",
							"required": true
                        },{
                            "id": "issue_Type",
						  "visibility": "null",
                          "order": 4,
                          "controlType": "dropdown",
                 	  	  "displayLabel": "I am trying to Enable replication, but",
                          "watermarkText": "Choose an option",
			"dropdownOptions":[{
				"value": "Push installation failed due to connectivity errors",
				"text": "Push installation failed due to connectivity errors"
			     },{
			    "value": "Push installation failure due to unsupported version",
				"text": "Push installation failure due to unsupported version"
			   },{
				"value": "Push installation failed due to boot/disc/root configurations",
				"text": "Push installation failed due to boot/disc/root configurations"
			 },{
			    "value": "Push installation failed due to VSS installation errors",
				"text": "Push installation failed due to VSS installation errors"
             },{
				"value": "Failed to register configuration server with my source machine",
				"text": "Failed to register configuration server with my source machine"
			 },{
			    "value": "Passphrase/invalid IP error",
				"text": "Passphrase/invalid IP error"
			   },{
				"value": "Configuration server is not connected",
				"text": "Configuration server is not connected"
			 },{
			    "value": "My initial replication is stuck",
				"text": "My initial replication is stuck"
             },{
				"value": "My issue isn't listed here",
				"text": "My issue isn't listed here"
			 }
			   ],
			   "required": true
            },{
			              "id": "learn_more_text",
                          "order": 5,
			  "visibility": "issue_Type == Push installation failed due to connectivity errors",
                          "controlType": "infoblock",
                          "content": "Most of the Push installation issues get resolved using our troubleshooting article, Try these <a href='https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-push-install'> troubleshooting steps</a> to self-resolve the issue."
            },{
			              "id": "learn_more_text",
                          "order": 6,
			  "visibility": "issue_Type == Push installation failure due to unsupported version",
                          "controlType": "infoblock",
                          "content": "<b>Ensure source machine has the <a href='https://docs.microsoft.com/azure/site-recovery/support-matrix-vmware-to-azure#replicated-machines'> supported Operating System/Kernel version</a> for successful installation of Mobility service."
            },{
			              "id": "learn_more_text",
                          "order": 7,
			  "visibility": "issue_Type == My initial replication is stuck",
                          "controlType": "infoblock",
                          "content": "Most of the initial replication issues get resolved using our troubleshooting article, Try these <a href='https://docs.microsoft.com/azure/site-recovery/vmware-azure-troubleshoot-replication#initial-replication-issues'> troubleshooting steps</a> to self-resolve the issue."
            }, {
                      "id": "problem_details",
                      "order": 8,
                        "visibility": "null",
                      "controlType": "multilinetextbox",
                       "displayLabel": "Please provide additional details:",
                      "watermarkText": "Paste error message(s), error code(s) and describe the scenario(s) that are failing.",
                      "required": true,
                      "useAsAdditionalDetails": true
        }
         ]}
---
                            
