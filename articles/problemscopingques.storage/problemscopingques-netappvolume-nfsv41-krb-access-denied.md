<properties
	articleId="problemscopingques-netappvolume-nfsv41-krb-access-denied"
	pageTitle="Getting Access Denied while Mounting the nfsv41 kerberos Volume"
	description="Getting Access Denied while Mounting the nfsv41 kerberos Volume"
	authors="b-mayada"
	ms.author="b-mayada"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32777910"
	productPesIds="16469"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureNetAppFiles"
/>
# Getting Access Denied while Mounting the nfsv41 kerberos Volume
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Getting Access Denied while Mounting the nfsv41 kerberos Volume",
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
			"id": "problem_description",
			"order": 2,
			"controlType": "multilinetextbox",
			"displayLabel": "Provide any additional details",
			"required": true,
			"useAsAdditionalDetails": true
		},
		{
            "id": "Volume_name",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Volume name",
            "watermarkText": "URI of the volume",
            "required": true
        },
		{
            "id": "a_ptr_record_for_dns",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Does a PTR record exist for the AD host machine in the everse lookup zone?",
            "watermarkText": "You need to create a reverse lookup zone on the DNS server, and then add a PTR record of the AD host machine in that reverse lookup zone",
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
                    "text": "I do not know"
                }
			],
            "required": false
        },
		{
            "id": "aes_256",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Is AES 256 encryption enabled for the machine accounts in the Active Directory?",
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
                    "text": "I do not know"
                }
			],
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---
