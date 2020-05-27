<properties
         pageTitle="Scoping questions for DPM issue configuring online backup"
         description="Scoping questions for DPM issue configuring online backup"
         authors="srinathvasireddy"
		 ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32553301"
         productPesIds="15207"
         cloudEnvironments="public, fairfax, usnat, ussec"
         schemaVersion="1"
		 articleId="449f9bd0-0f11-422d-ac3a-3024cf49fd57"
	ownershipId="StorageMediaEdge_Backup"
/>
# Questions DPM issue configuring online backup
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "DPM issue configuring online backup",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "DPM issue configuring online backup",
        "description": "These diagnostics will check for errors.",
        "insightNotAvailableText": "We didn't find any problems"
    },
    "formElements": [
        {
            "id": "os_version",
	    "visibility": "null",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "What is the OS version of the impacted system?",
            "watermarkText": "ex. Windows 2012 R2",
            "required": false
        },
        {
            "id": "machine_name",
	    "visibility": "null",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Which machine is experiencing the problem?",
            "watermarkText": "Enter the name of the Windows Server or Windows Client",
            "required": false
        },
        {
            "id": "error_message",
	    "visibility": "null",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Provide the error message that are you seeing:",
            "watermarkText": "Copy and paste error message text from failed job details dialog in Microsoft Azure Backup agent",
            "required": false
        },
        {
            "id": "registration_type",
	    "visibility": "null",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "At what stage of configuring or enabling backup are you facing the issue?",
            "watermarkText": "Select",
            "dropdownOptions": [
                {
                    "value": "Installing/upgrading DPM",
                    "text": "Installing/upgrading DPM"
                },
                {
                    "value": "Installing/upgrading Azure Backup Server",
                    "text": "Installing/upgrading Azure Backup Server"
                },
                {
                    "value": "Registering DPM to Recovery Services Vault",
                    "text": "Registering DPM to Recovery Services Vault"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true,
     "diagnosticInputRequiredClients": "Portal"
        },
	{
	   "id": "issue_type",
            "visibility": "registration_type == Registering DPM to Recovery Services Vault",
            "order": 5,
            "controlType": "dropdown",
	    "infoBalloonText": "Check installation and registration <a href='https://aka.ms/AB-AA4dp4y'>Troubleshooting</a> article",
            "displayLabel": "Which type of issue you are facing?",
            "dropdownOptions": [
                {
                    "value": "Proxy Configuration failed",
                    "text": "Proxy Configuration failed"
                },
                {
                    "value": "Installing pre-requisites (.NET and PowerShell) failed",
                    "text": "Installing pre-requisites (.NET and PowerShell) failed"
                },
                {
                    "value": "Issue with Vault Credentials",
                    "text": "Issue with Vault Credentials"
                },
                {
                    "value": "Issue with encryption-key/passphrase",
                    "text": "Issue with encryption-key/passphrase"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
		},
        {
            "id": "basic_troubleshooting_multiselect",
            "visibility": "registration_type == Registering DPM to Recovery Services Vault",
            "order": 6,
            "controlType": "multiselectdropdown",
            "displayLabel": "Select the troubleshooting steps you have performed:",
            "dropdownOptions": [
                {
                    "value": "OS version is supported for backup",
                    "text": "OS version is supported for backup"
                },
                {
                    "value": "If firewall is used, then required URLs are whitelisted",
                    "text": "If firewall is used, then required URLs are whitelisted"
                },
                {
                    "value": "Machine has Internet connectivity",
                    "text": "Machine has Internet connectivity"
                },
                {
                    "value": "If antivirus is running, then exclusion rules are used",
                    "text": "If antivirus is running, then exclusion rules are used"
                },
                {
                    "value": ".NET framework version is at least 4.6.2",
                    "text": ".NET framework version is at least 4.6.2"
                },
                {
                    "value": "Server is not registered with another vault",
                    "text": "Server is not registered with another vault"
                },
                {
                    "value": "Ensure c:/windows/temp folder has less than 60,000 files",
                    "text": "Ensure c:/windows/temp folder has less than 60,000 files"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 7,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "hints": []
        },
        {
            "id": "problem_start_time",
	    "visibility": "null",
            "order": 8,
            "controlType": "datetimepicker",
            "displayLabel": "Problem start time",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
