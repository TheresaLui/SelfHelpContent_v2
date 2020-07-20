<properties pageTitle="Problem with AAD Connect install/upgrade" 
	 description="aadconnectinstallationandupgrade" 
	 authors="anupnadigm" 
	 selfHelpType="problemScopingQuestions" 
	 supportTopicIds="32404460" 
	 productPesIds="14785,16578" 
	 cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec" 
	 schemaVersion="1"
    articleId="d57b0cb3-558b-4448-a05e-ad09318d72b4"
	ownershipId="AzureIdentity_DirectoryObjectManagement"
/> 
# Problem with AAD Connect install/upgrade 
---
{
    "resourceRequired": false,
    "title": "Problem with AAD Connect install/upgrade",
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
                    "text": "Uninstallation",
                    "value": "uninstallation"
                },
                {
                    "text": "Automatic Upgrade",
                    "value": "autoUpgrade"
                },
                {
                    "text": "Upgrade from previous version (in-place upgrade)",
                    "value": "upgradeInplace"
                },
                {
                    "text": "Upgrade from previous version (swing or side-by-side migration)",
                    "value": "upgradeSwing"
                },
                {
                    "text": "Upgrade from DirSync (in-place upgrade)",
                    "value": "upgradeDirSyncInplace"
                },
                {
                    "text": "Upgrade from DirSync (parallel deployment)",
                    "value": "upgradeDirSyncParallel"
                },
                {
                    "text": "Upgrade from Azure AD Sync (in-place upgrade)",
                    "value": "upgradeAADSyncInPlace"
                },
                {
                    "text": "Upgrade from Azure AD Sync (swing or side-by-side migration)",
                    "value": "upgradeAADSyncSwing"
                },
                {
                    "text": "Other",
                    "value": "otherProblem"
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
            "id": "otherProblemDescribe",
            "visibility": "problem==otherProblem",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Problem (other)",
            "content": null,
            "watermarkText": "Please describe the problem you have.",
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "hints": [],
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 3
        },
        {
            "id": "symptoms",
            "visibility": "true",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "What are the symptoms?",
            "content": null,
            "watermarkText": "Please describe any symptoms and error messages encountered.",
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "hints": [],
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 3
        },
        {
            "id": "problem_start_time",
            "visibility": null,
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem occur?",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "hints": [],
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "filesToUpload",
            "visibility": "true",
            "order": 5,
            "controlType": "infoblock",
            "displayLabel": null,
            "content": "Please provide a copy of the '%programdata%\\AADConnect' folder from the Azure AD Connect server. Put all the content to be shared into a single ZIP file and upload the file using 'File upload' on the left.",
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "hints": [],
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "problem_description",
            "visibility": null,
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional details",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "hints": null,
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": true,
            "numberOfLines": 0
        }
    ],
    "$schema": "SelfHelpContent"
}
---