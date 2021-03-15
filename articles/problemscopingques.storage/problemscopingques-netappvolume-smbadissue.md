<properties
	articleId="problemscopingques-netappvolume-SMBADIssue"
	pageTitle="Issues with DNS and Active Directory"
	description="Issues with DNS and Active Directory"
	authors="b-avaish"
    ms.author="b-avaish"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32740758"
	productPesIds="16469"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureNetAppFiles"
/>
# Issues with DNS and Active Drectory
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Issues with SMB Volumes,DNS,Active Directory",
    "fileAttachmentHint": "",
    "formElements": [
		{
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
        {
            "id": "nfsvolumetype",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What is the volume type?",
            "watermarkText": "(i.e. SMB, Dual Protocol, NFSv3, NFSv4.1, NFSv4.1 Kerberos)",
            "dropdownOptions": [{
                    "value": "SMB",
                    "text": "SMB"
                },
                {
                    "value": "Dual Protocol",
                    "text": "Dual Protocol"
                },
                {
                    "value": "NFSv3",
                    "text": "NFSv3"
                },
                {
                    "value": "NFSv4.1",
                    "text": "NFSv4.1"
                },
                {
                    "value": "NFSv4.1 Kerberos",
                    "text": "NFSv4.1 Kerberos"
                },
                {
                    "value": "dont_know_answer",
                    "text": "None of the above"
                }
            ],
            "required": true
        },
        {
            "id": "error_message",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Error message received",
            "required": false
        },
        {
            "id": "SMBADIssue",
            "order": 3,
            "ControlType": "dropdown",
            "displayLabel": "Is the username provided in the security privilege block the same as the domain username used for installing Microsoft SQL server?",
            "watermarkText": "Is the username given in security privilege block same as domain username used for installing Microsoft SQL server?",
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
        },
        {
            "id": "ADconnection_config",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide details on the AD connection configuration",
            "watermarkText": "(i.e. AES Encryption, LDAP Signing, LDAP over TLS, Allow local NFS users with LDAP, etc.)",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide any additional details",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
