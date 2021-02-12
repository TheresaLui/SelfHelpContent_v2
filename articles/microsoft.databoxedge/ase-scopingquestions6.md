<properties
	pageTitle="Scoping Questions for Azure Stack Edge Certificates"
	description="Scoping Questions for Azure Stack Edge Certificates"
	authors="hadhand"
	ms.author="hadhand"
	authoralias="hadhand"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32745978"
	productPesIds="16597"
	cloudEnvironments="public, Fairfax, mooncake, blackforest, usnat, ussec"
	schemaVersion="1"
	articleId="CertificatesScopingQuesASE"
	ownershipId="StorageMediaEdge_DataBox"
/>

# Data Box Edge issues with setup and configuration
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Azure Stack Edge issues",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When was the problem first observed?",
            "required": true
        },
	{
	     "id": "Verify Certificates",
	     "order": 200,
	     "controlType": "dropdown",
	     "displayLabel": "If you are using device certificate make sure, the certificate is valid and not expired.",
             "watermarkText": "Choose an option",
             "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Do not know"
                },
                {
                    "value": "already_done",
                    "text": "Have already done"
                }
	    ],
            "required": true
        },
	{
	     "id": "BYOC",
	     "order": 300,
	     "controlType": "dropdown",
	     "displayLabel": "In case of BYOC, then make sure we are having the signing root certificate along with rest of the certificates",
             "watermarkText": "Choose an option",
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
                    "text": "Do not know"
                }
	    ],
            "required": true
        },
	{
	     "id": "Comply Certificates",
	     "order": 400,
	     "controlType": "dropdown",
	     "displayLabel": " Comply with the format of the certificates which needs to be uploaded?",
             "watermarkText": "Choose an option",
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
                    "text": "Do not know"
                }
	    ],
            "required": true
        },
        {
            "id": "problem_description",
            "order": 600,
            "controlType": "multilinetextbox",
            "displayLabel": "Additional details about the issue",
            "watermarkText": "Please provide the details regarding the issue, such as Error that you are getting.",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "learn_more_text",
            "order": 700,
            "controlType": "infoblock",
            "content": "<a href='https://docs.microsoft.com/azure/databox-online/azure-stack-edge-connect-powershell-interface#upload-certificate'>Learn more</a> about Azure Stack Edge Certificates"
        }
	],
	"$schema": "SelfHelpContent"
}
---
