<properties
         pageTitle="Scoping questions for unable to (Re)register to vault"
         description="Scoping questions for unable to (Re)register to vault"
         authors="srinathv"
	 ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32632798"
         productPesIds="15207"
         cloudEnvironments="public"
         schemaVersion="1"
	 articleId="66f2b938-2ad1-450f-9622-6572bda040c8"
/>
# Questions for unable to (Re)register to vault
---
{
         "resourceRequired": true,
	 "subscriptionRequired": true,
         "title": "unable to (Re)register to vault",
         "fileAttachmentHint": "",
         "formElements":[{
                "id": "machine_name",
                "order": 1,
                "controlType": "textbox",
                "displayLabel": "Which machine is experiencing the problem?",
                "watermarkText": "Enter the name of the Windows Server or Windows Client",
                "required": true
        },{
                "id": "error_message",
                "order": 2,
                "controlType": "textbox",
                "displayLabel": "Provide the error message that are you seeing:",
                "watermarkText": "Copy and paste error message text here",
                "required": false
	},{
                "id": "vault_name",
                "order": 3,
                "controlType": "textbox",
                "displayLabel": "Provide the vault name in which you are trying to (Re)register machine",
                "watermarkText": "ex. contoso_vault",
                "required": false
	},{
              "id": "basic_troubleshooting_multiselect",
              "order": 4,
              "controlType": "multiselectdropdown",
              "infoBalloonText": "Check Azure Backup agent <a href='https://aka.ms/AB-AA4dp4y'>Troubleshooting</a> article",
              "displayLabel": "Select the troubleshooting steps that you have performed:",
              "dropdownOptions": [{
		      "value": "Ensured Azure Backup agent is latest",
                      "text": "Ensured Azure Backup agent is latest"
                },{
                      "value": "Machine has Internet connectivity",
                      "text": "Machine has Internet connectivity"
                },{
                      "value": "Try register using latest vault credential file",
                      "text": "Try register using latest vault credential file"
		},{
                      "value": "Tried registering with a vault credentials downloaded within 48hrs",
                      "text": "Tried registering with a vault credentials downloaded within 48hrs"
		},{
                      "value": "Firewall settings on the machine/proxy are configured to allow required URLs",
                      "text": "Firewall settings on the machine/proxy are configured to allow required URLs"
		},{
                      "value": "If proxy is enabled, then browser settings are configured to use proxy",
                      "text": "If proxy is enabled, then browser settings are configured to use proxy"
	        },{
                      "value": "If antivirus is running, then exclusion rules are used",
                      "text": "If antivirus is running, then exclusion rules are used"
                },{
                    "value": "Ensured machine is not registered with an another vault",
                    "text": "Ensured machine is not registered with an another vault"
                },{
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
          ],
          "required": true
	    },{
              "id": "problem_start_time",
              "order": 5,
              "controlType": "datetimepicker",
              "displayLabel": "When did the problem begin?",
              "required": true
	    },{
              "id": "problem_description",
              "order": 6,
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
