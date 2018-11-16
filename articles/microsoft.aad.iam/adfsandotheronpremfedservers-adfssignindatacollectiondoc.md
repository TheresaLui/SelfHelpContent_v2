<properties pageTitle="Problem with ADFS sign in" 
	 description="adfssignindatacollectiondoc" 
	 authors="anupnadigm" 
	 selfHelpType="problemScopingQuestions" 
	 supportTopicIds="32570971" 
	 productPesIds="14785" 
	 cloudEnvironments="public" 
	 schemaVersion="1"
/> 
# Problem with ADFS sign in 
---
{
  "resourceRequired": false,
  "title": "Problem with ADFS sign in",
  "fileAttachmentHint": null,
  "formElements": [
    {
      "id": "userUPN",
      "visibility": null,
      "order": 1,
      "controlType": "multilinetextbox",
      "displayLabel": "UPN of one of the affected users?",
      "content": null,
      "watermarkText": "Example: user@contoso.com",
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
      "id": "isMultipleDomain",
      "visibility": null,
      "order": 2,
      "controlType": "dropdown",
      "displayLabel": "Are multiple domains federated with the AD FS farm?",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": [
        {
          "text": "Yes",
          "value": "MultiDomainFederation"
        },
        {
          "text": "No",
          "value": "SingleDomainFederation"
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
      "id": "allUsersImpacted",
      "visibility": null,
      "order": 3,
      "controlType": "dropdown",
      "displayLabel": "Are all users impacted?",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": [
        {
          "text": "Yes",
          "value": "AllUsersImpacted"
        },
        {
          "text": "No",
          "value": "SingleOrSelectedUsersImpacted"
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
      "id": "AreaOfImpact",
      "visibility": null,
      "order": 4,
      "controlType": "dropdown",
      "displayLabel": "Internal / external authentication impacted?",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": [
        {
          "text": "Internal (within corpnet)",
          "value": "Internal"
        },
        {
          "text": "External (via WAP)",
          "value": "External"
        },
        {
          "text": "Both Internal and External",
          "value": "BothInternalExternal"
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
      "id": "whereIsError",
      "visibility": null,
      "order": 5,
      "controlType": "dropdown",
      "displayLabel": "Where is the error reported during sign-in?",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": [
        {
          "text": "At AD FS Sign-in Page",
          "value": "ErrorOnAdfsPage"
        },
        {
          "text": "Somewhere in the Application",
          "value": "ErrorOnApplicationPage"
        },
        {
          "text": "I don't know",
          "value": "NotSureErrorLocation"
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
  ]
}
---