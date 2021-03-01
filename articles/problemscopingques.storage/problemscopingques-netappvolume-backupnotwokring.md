<properties
	articleId="problemscopingques-netappvolume-backupnotworking"
<<<<<<< HEAD
	pageTitle="Backup not working after policy assignment"
	description="Backup not working after policy assignment"
	authors="b-avaish"
	ms.author="b-avaish"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32784804"
=======
	pageTitle="Backup not working after backup policy assignment"
	description="Backup not working after backup policy assignment"
	authors="b-avaish"
	ms.author="b-avaish"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32781859"
>>>>>>> b12d42114166b55c039e3acb382fadca73b4edc7
	productPesIds="16469"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureNetAppFiles"
/>
<<<<<<< HEAD
# Backup not working after policy assignment
=======
# Backup not working after backup policy assignment
>>>>>>> b12d42114166b55c039e3acb382fadca73b4edc7
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
<<<<<<< HEAD
    "title": "Backup not working after policy assignment",
=======
    "title": "Backup not working after backup policy assignment",
>>>>>>> b12d42114166b55c039e3acb382fadca73b4edc7
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
            "id": "policy_state",
            "order": 2,
            "controlType": "dropdown",
<<<<<<< HEAD
            "displayLabel": "Are the policy state of assigned backup policy and snapshot policy enabled?",
            "watermarkText": "Are the policy state of assigned backup policy and snapshot policy enabled?",
=======
            "displayLabel": "Is the backup policy state enable?",
            "watermarkText": "Is the backup policy state enable?",
>>>>>>> b12d42114166b55c039e3acb382fadca73b4edc7
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
<<<<<<< HEAD
        "id": "configure_backups",
        "order": 3,
        "controlType": "dropdown",
        "displayLabel": "What is the policy state in configure backups of a volume",
        "watermarkText": "Choose an option",
        "dropdownOptions": [{
            "value": "Suspend",
            "text": "Suspend"
        }, {
            "value": "Resume",
            "text": "Resume"
=======
        "id": "snapshot_policy",
        "order": 3,
        "controlType": "dropdown",
        "displayLabel": "Is the snapshot policy assigned to volume?",
        "watermarkText": "Is the snapshot policy assigned to volume?",
        "dropdownOptions": [{
            "value": "Yes",
            "text": "Yes"
        }, {
            "value": "No",
            "text": "No"
>>>>>>> b12d42114166b55c039e3acb382fadca73b4edc7
        }, {
            "value": "dont_know_answer",
            "text": "None of the above"
        }],
        "required": true
	},
	{
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
<<<<<<< HEAD
---
=======
---
>>>>>>> b12d42114166b55c039e3acb382fadca73b4edc7
