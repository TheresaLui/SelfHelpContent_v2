<properties pageTitle="Problem with AAD Connect install/upgrade" 
	 description="aadconnectinstallationandupgrade" 
	 authors="anupnadigm" 
	 selfHelpType="problemScopingQuestions" 
	 supportTopicIds="32404460" 
	 productPesIds="14785" 
	 cloudEnvironments="public" 
	 schemaVersion="1"
/> 
# Problem with AAD Connect install/upgrade 
---
{
  "resourceRequired": true,
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
      "id": "whenOccurred",
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
      "displayLabel": "Please provide a copy of the '%programdata%\\\\AADConnect' folder from the Azure AD Connect server. Put all the content to be shared into a single ZIP file and upload the file using 'File upload' on the left.",
      "content": "<a href='#'>Please provide a copy of the '%programdata%\\\\AADConnect' folder from the Azure AD Connect server. Put all the content to be shared into a single ZIP file and upload the file using 'File upload' on the left.</a>",
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
      "id": "aadConnectInstallationAndUpgradeadditionalDetails",
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
  ]
}
---