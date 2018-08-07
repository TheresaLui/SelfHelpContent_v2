<properties pageTitle="Problem with Activity logs in Azure AD" 
	 description="issuesactivitylogsaad" 
	 authors="anupnadigm" 
	 selfHelpType="problemScopingQuestions" 
	 supportTopicIds="32574687" 
	 productPesIds="14785" 
	 cloudEnvironments="public" 
	 schemaVersion="1"
/> 
# Problem with Activity logs in Azure AD 
---
{
  "resourceRequired": true,
  "title": "Problem with Activity logs in Azure AD",
  "fileAttachmentHint": null,
  "formElements": [
    {
      "id": "Whichenv",
      "visibility": null,
      "order": 1,
      "controlType": "dropdown",
      "displayLabel": "Which environment are you using?",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": [
        {
          "text": "Azure Portal",
          "value": "AP"
        },
        {
          "text": "Azure AD Logs through Diagnostics Settings",
          "value": "AMD"
        },
        {
          "text": "O365 Admin Portal",
          "value": "O365"
        },
        {
          "text": "Microsoft Graph APIs",
          "value": "API"
        },
        {
          "text": "Azure AD Power BI Content Pack",
          "value": "PBI"
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
      "id": "dataretention",
      "visibility": "whichenv==AP",
      "order": 2,
      "controlType": "infoblock",
      "displayLabel": null,
      "content": "You are currently using Azure portal",
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
      "id": "whichactivity",
      "visibility": null,
      "order": 3,
      "controlType": "dropdown",
      "displayLabel": "Which activity data are you having problem with?",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": [
        {
          "text": "Sign-ins",
          "value": "signins"
        },
        {
          "text": "Audit",
          "value": "audit"
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
      "id": "Whichissue",
      "visibility": null,
      "order": 4,
      "controlType": "dropdown",
      "displayLabel": "What issue is this related to?",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": [
        {
          "text": "I can't find all the activity logs in my downloaded/exported file",
          "value": "missingdatadownload"
        },
        {
          "text": "I can't find actions that have been recently performed in Azure AD through activity logs",
          "value": "latencydata"
        },
        {
          "text": "I can't find activity logs beyond 30 days (Premium tenants) or 7 days (free/basic tenants)",
          "value": "dataretention_free"
        },
        {
          "text": "Other issues",
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
      "id": "dataretention2",
      "visibility": "tenantSubscription!=yes",
      "order": 5,
      "controlType": "infoblock",
      "displayLabel": null,
      "content": "Check out the frequently asked questions about Activity logs here.",
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
      "id": "whenBegan",
      "visibility": null,
      "order": 6,
      "controlType": "datetimepicker",
      "displayLabel": "When did the problem begin? (Provide Date in UTC format)",
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
      "id": "symptoms",
      "visibility": null,
      "order": 7,
      "controlType": "multilinetextbox",
      "displayLabel": "What is the RequestId (for Sign-ins) and CorrelationId (for audit)?",
      "content": null,
      "watermarkText": null,
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
      "id": "symptoms2",
      "visibility": null,
      "order": 8,
      "controlType": "multilinetextbox",
      "displayLabel": "What are the symptoms of the problem?",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": [],
      "required": true,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 4
    },
    {
      "id": "IssuesActivitylogsAADadditionalDetails",
      "visibility": null,
      "order": 9,
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