<properties pageTitle="Other problem with licenses" 
	 description="problemotherlicensingissues" 
	 authors="anupnadigm" 
	 selfHelpType="problemScopingQuestions" 
	 supportTopicIds="32570962" 
	 productPesIds="14785" 
	 cloudEnvironments="public" 
	 schemaVersion="1"
/> 
# Other problem with licenses 
---
{
  "resourceRequired": false,
  "title": "Other problem with licenses",
  "fileAttachmentHint": null,
  "formElements": [
    {
      "id": "infoAzureSubscriptions",
      "visibility": "true",
      "order": 1,
      "controlType": "infoblock",
      "displayLabel": null,
      "content": "<a href='https://docs.microsoft.com/azure/active-directory/active-directory-how-subscriptions-associated-directory'>Note that this problem type is about per-user subscriptions such as Office 365, Azure AD Premium, Enterprise Mobility + Security, etc. If your issue is related to Azure resourec subscriptions (e.g. granting access to Azure resources in a subscription), please choose Problem type: Subscription problems.</a>",
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
      "id": "whereProblem",
      "visibility": null,
      "order": 2,
      "controlType": "dropdown",
      "displayLabel": "What environment are you using to manage licenses?",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": [
        {
          "text": "Azure portal",
          "value": "azurePortal"
        },
        {
          "text": "Office portal",
          "value": "officePortal"
        },
        {
          "text": "PowerShell cmdlets",
          "value": "powerShell"
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
      "order": 3,
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
      "order": 4,
      "controlType": "infoblock",
      "displayLabel": null,
      "content": "<a href='https://docs.microsoft.com/azure/active-directory/active-directory-licensing-group-advanced#direct-licenses-coexist-with-group-licenses'>When users inherit licenses from groups it may not be possible to modify or remove the license from a user. Azure portal displays useful error details in such cases - make sure to click the error notification when your operation fails to find out more. Click here to read about group-based licensing.</a>",
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
      "id": "symptoms",
      "visibility": null,
      "order": 5,
      "controlType": "multilinetextbox",
      "displayLabel": "What are the symptoms of the problem?",
      "content": null,
      "watermarkText": "Additional details that might help us diagnose and solve the problem, such as the name of the product license you are assigning. Consider clicking on the error notification in the portal to display full information about the problem and copy the error details.",
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
      "id": "problem_description",
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