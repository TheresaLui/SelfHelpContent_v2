<properties
    pageTitle="Problem with dynamic groups"
    description="problemwithdynamicgroups"
    authors="anupnadigm"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32570978"
    productPesIds="14785,16578,16575"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    schemaVersion="1"
     articleId="aa2fdaba-eb64-4593-bf36-ae4f4a212c8c"
    	ownershipId="AzureIdentity_DirectoryObjectManagement"
/>

# Problem with dynamic groups

---
{
    "resourceRequired": false,
    "title": "Problem with dynamic groups",
    "fileAttachmentHint": null,
    "formElements": [
        {
            "id": "groupId",
            "visibility": null,
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the Object ID of the group you are having problems with?",
            "content": null,
            "watermarkText": "The Object ID can be found by opening the group in the portal, in the Overview tab in the Essentials box on the very top.",
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "hints": [],
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 2
        },
        {
            "id": "membershipRule",
            "visibility": null,
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the membership rule you are having problems with?",
            "content": null,
            "watermarkText": "Open the group in the portal, click \"Dynamic membership rules\" and click \"Advanced Rule\" and copy the contents here.",
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "hints": [],
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 2
        },
        {
            "id": "problemUserOrDevice",
            "visibility": null,
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Object ID of the user or device that is not showing up in the dynamic group:",
            "content": null,
            "watermarkText": "If you believe a particular user or device should be a member of the dynamic group but is missing, please provide the object ID for the user or device.",
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "hints": [],
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 2
        },
        {
            "id": "problem_start_time",
            "visibility": null,
            "order": 4,
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
            "id": "symptoms",
            "visibility": null,
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "What are the symptoms of the problem?",
            "content": null,
            "watermarkText": "Tell us what you are trying to accomplish and what is not working.",
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "hints": [],
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 4
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
