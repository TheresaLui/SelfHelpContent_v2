<properties pageTitle="Problem assigning licenses to a group" 
description="Problem assigning licenses to a group" 
authors="anmalath" 
selfHelpType="problemassigninglicensetoagroup" 
supportTopicIds="32570958" 
productPesIds="14785" 
cloudEnvironments="public" 
schemaVersion="1"/>

{
  "resourceRequired": true,
  "title": "Problem assigning licenses to a group",
  "fileAttachmentHint": null,
  "formElements": [
    {
      "id": "tenantSubscription",
      "visibility": null,
      "order": 1,
      "controlType": "dropdown",
      "displayLabel": "Does the tenant have a subscription for a premium Azure AD product?",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": null,
      "required": true,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 0
    },
    {
      "id": "licenseRequirement",
      "visibility": "tenantSubscription!=yes",
      "order": 2,
      "controlType": "infoblock",
      "displayLabel": "Assigning licenses to groups is currently in Public Preview and requires an active subscription for one of the Azure AD products, such as: Azure AD Basic, Azure AD Premium, or Enterprise Mobility + Security. You can see the list of your subscriptions under Azure Active Directory->Licenses->All Products. Click here to read more about the preview and the license requirement to use this feature.",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": null,
      "required": false,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 0
    },
    {
      "id": "whereProblem",
      "visibility": null,
      "order": 3,
      "controlType": "dropdown",
      "displayLabel": "What environment are you using to assign a license to a group?",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": null,
      "required": true,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 0
    },
    {
      "id": "portalAvailability",
      "visibility": "whereProblem!=azurePortal",
      "order": 4,
      "controlType": "infoblock",
      "displayLabel": "Assigning licenses to groups is only available through the Azure portal. Open the group in the portal, go to the Licenses tab to view or modify a license on a group. Click here to find out more.",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": null,
      "required": false,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 0
    },
    {
      "id": "groupId",
      "visibility": null,
      "order": 5,
      "controlType": "multilinetextbox",
      "displayLabel": "What is the Object ID of the group you are having problems with?",
      "content": null,
      "watermarkText": "The Object ID can be found by opening the group in the portal, in the Overview tab in the Essentials box on the very top.",
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": null,
      "required": true,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 2
    },
    {
      "id": "symptoms",
      "visibility": null,
      "order": 6,
      "controlType": "multilinetextbox",
      "displayLabel": "What are the symptoms of the problem?",
      "content": null,
      "watermarkText": "Tell us what you are trying to accomplish and what is not working.",
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": null,
      "required": true,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 4
    },
    {
      "id": "whenBegan",
      "visibility": null,
      "order": 7,
      "controlType": "datetimepicker",
      "displayLabel": "When did the problem begin?",
      "content": null,
      "watermarkText": null,
      "infoBalloonText": null,
      "dropdownOptions": null,
      "dynamicDropdownOptions": null,
      "hints": null,
      "required": false,
      "maxLength": 0,
      "useAsAdditionalDetails": false,
      "numberOfLines": 0
    },
    {
      "id": "problemAssigningLicenseToAGroupadditionalDetails",
      "visibility": null,
      "order": 8,
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