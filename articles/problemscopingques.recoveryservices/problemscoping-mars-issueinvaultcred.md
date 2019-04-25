<properties
         pageTitle="Scoping questions for issue in vault credential download"
         description="Scoping questions for issue in vault credential download"
         authors="srinathv"
		     ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32632797"
         productPesIds="15207"
         cloudEnvironments="public"
         schemaVersion="1"
		     articleId="2e956193-880f-437c-942e-575465e86ce2"
/>
# Questions for issue in vault credential download
---
{
         "resourceRequired": true,
		     "subscriptionRequired": true,
         "title": "Issue in vault credential download",
         "fileAttachmentHint": "",
         "formElements":[{
                    "id": "error_message",
                    "order": 1,
                    "controlType": "textbox",
                    "displayLabel": "Provide the error message that are you seeing:",
                    "watermarkText": "Copy and paste error message text here",
                    "required": false
	    	},{
                    "id": "vault_name",
                    "order": 2,
                    "controlType": "textbox",
                    "displayLabel": "Provide the vault name from which you are trying to download vault credential",
                    "watermarkText": "ex. contoso_vault",
                    "required": false
	    	},{			
                    "id": "basic_troubleshooting_multiselect",
                    "order": 3,
                    "controlType": "multiselectdropdown",
                    "infoBalloonText": "Check Azure Backup agent<a href='https://aka.ms/AAB-unable-to-download-vault-credential-file'>Troubleshooting</a> article",
                    "displayLabel": "Select the troubleshooting steps that you have performed:",
                    "dropdownOptions": [{
                                            "value": "Try to download vault credential file using different browser",
                                            "text": "Try to download vault credential file using different browser"
                                      },{
                                            "value": "Ensure the subscription is not disabled/expired",
                                            "text": "Ensure the subscription is not disabled/expired"
                                      },{
                                            "value": "Ensure there is no any firewall rule blocking vault credential file to download",
                                            "text": "Ensure there is no any firewall rule blocking vault credential file to download"
                                      },{
                                            "value": "Ensure the vault limit (50 machines per vault) is not exhausted",
                                            "text": "Ensure the vault limit (50 machines per vault) is not exhausted"
                                      },{
                                            "value": "Ensure user has required Azure Backup permission to download vault credential",
                                            "text": "Ensure user has required Azure Backup permission to download vault credential"
                                      },{
                                            "value": "dont_know_answer",
                                            "text": "Other, don't know or not applicable"
                                         }
                                      ],
                                      "required": true
	        },{
                  "id": "problem_start_time",
                  "order": 3,
                  "controlType": "datetimepicker",
                  "displayLabel": "When did the problem begin?",
                  "required": true
	       },{
                  "id": "problem_description",
                  "order": 4,
                  "controlType": "multilinetextbox",
                  "useAsAdditionalDetails": true,
                  "displayLabel": "Additional details",
                  "watermarkText": "Provide additional information about your issue",
                  "required": true,
                  "hints": []
			      }
	   	]
}
---
