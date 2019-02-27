<properties
	pageTitle="Azure Information Protection - Scanner Installation"
	description="Azure Information Protection - Scanner Installation"
	service="microsoft.aip"
	resource="aip"
	authors="orbarak-ms"
	ms.author="orbarak"
	articleId="Scanner_Installation"
	displayOrder=""
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32629559"
	resourceTags=""
	productPesIds="14997"
	cloudEnvironments="public"
    schemaVersion="1"
/>

# Azure Information Protection - Scanner Installation
---
{
    "resourceRequired": false,
    "title": "Problem with AIP Scanner install/upgrade",
    "fileAttachmentHint": "Upload the ZIP file",
    "formElements": [
        {
            "id": "problem",
            "visibility": "true",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "What problem are you having",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "New installation",
                    "value": "installation"
                },
                {
                    "text": "Upgrade",
                    "value": "upgrade"
                }
            ],
            "dynamicDropdownOptions": null,
            "hints": [],
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
		{
            "id": "upgradeproblem",
            "order": 2,
            "visibility": "problem == upgrade",   
            "controlType": "dropdown",
            "displayLabel": "Did you run Update-AIPScanner? <a href='https://docs.microsoft.com/azure/information-protection/rms-client/client-admin-guide#upgrading-the-azure-information-protection-scanner)'>upgrading the Azure Information Protection scanner</a>",
            "watermarkText": "Choose an option",
            "dropdownOptions": [{
                    "value": "yes",
                    "text": "yes"
                },{
                    "value": "no",
                    "text": "no"
                }],
            "required": true
        },
        {
            "id": "filesToUpload",
            "visibility": "true",
            "order": 3,
            "controlType": "infoblock",
            "displayLabel": null,
            "content": "Please provide a copy of the '%localappdata%\\\\Microsoft\\\\MSIP' folder from the server running AIP Scanner. Put all the content to be shared into a single ZIP file and upload the file using 'File upload' on the left.",
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "hints": [],
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        }
    ]
}
---


