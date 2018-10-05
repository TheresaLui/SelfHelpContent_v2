<properties pageTitle="Problem with licenses using powershell" 
	 description="problemassigninglicenseusingpowershell" 
	 authors="anupnadigm" 
	 selfHelpType="problemScopingQuestions" 
	 supportTopicIds="32570960" 
	 productPesIds="14785" 
	 cloudEnvironments="public" 
	 schemaVersion="1"
/> 
# Problem with licenses using powershell 
---
{
  "resourceRequired": false,
  "title": "Problem with licenses using powershell",
  "fileAttachmentHint": null,
  "formElements": [
    {
      "id": "apisUsed",
      "visibility": null,
      "order": 1,
      "controlType": "dropdown",
      "displayLabel": "What version of PowerShell are you using?",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": [
        {
          "text": "Azure AD PowerShell v1 (e.g. Set-​Msol​User​License)",
          "value": "v1"
        },
        {
          "text": "Azure AD PowerShell v2 (e.g. Set-​Azure​AD​User​License)",
          "value": "v2"
        },
        {
          "text": "Microsoft Graph APIs",
          "value": "msGraph"
        },
        {
          "text": "Not sure",
          "value": "other"
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
      "id": "gblUse",
      "visibility": null,
      "order": 2,
      "controlType": "dropdown",
      "displayLabel": "Are you using group-based licensing in your tenant to automate license assignment to users?",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": [
        {
          "text": "Yes",
          "value": "yes"
        },
        {
          "text": "No",
          "value": "no"
        },
        {
          "text": "Not sure",
          "value": "dontknow"
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
      "id": "gblAndDirectAssignment",
      "visibility": "gblUse!=no",
      "order": 3,
      "controlType": "infoblock",
      "displayLabel": null,
      "content": "<a href='https://docs.microsoft.com/azure/active-directory/active-directory-licensing-ps-examples'>Group-based licensing is currently in preview and has limited support via PowerShell and Graph APIs. Click here to read more about how PowerShell v1 cmdlets can be used with this feature.</a>",
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
      "id": "psCmdlet",
      "visibility": null,
      "order": 4,
      "controlType": "multilinetextbox",
      "displayLabel": "What is the PowerShell cmdlet that you are executing?",
      "content": null,
      "watermarkText": "Please copy the cmdlet you are executing. Make sure not to include any data you don't want to share, such as your credentials.",
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": [],
      "required": true,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 2
    },
    {
      "id": "symptoms",
      "visibility": null,
      "order": 5,
      "controlType": "multilinetextbox",
      "displayLabel": "What are the symptoms of the problem?",
      "content": null,
      "watermarkText": "Additional details that might help us diagnose and solve the problem. For example, the error output from PowerShell.",
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": [],
      "required": true,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 2
    },
    {
      "id": "whenBegan",
      "visibility": null,
      "order": 6,
      "controlType": "datetimepicker",
      "displayLabel": "When did the problem begin?",
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
      "id": "problemAssigningLicenseUsingPowerShelladditionalDetails",
      "visibility": null,
      "order": 7,
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