<properties
    pageTitle="Problem assigning licenses to a group"
    description="problemassigninglicensetoagroup"
    authors="chpate"
    ms.authors="chpate"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32570958,32615386"
    productPesIds="14785,16578,16575,16578"
    cloudEnvironments="public"
    schemaVersion="1"
    articleId="23c1cf4d-6fdd-475b-ba06-87595b53195b"
    />

# Problem assigning licenses to a group

---
{
    "resourceRequired": false,
    "title": "Problem assigning licenses to a group",
    "fileAttachmentHint": null,
    "formElements": [
        {
            "id": "purchaseOrUpgrade",
            "visibility": null,
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Is your question regarding purchase/upgrade of license (including trial)?",
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
            "id": "purchaseOrUpgradeSelected",
            "visibility": "purchaseOrUpgrade!=no",
            "order": 2,
            "controlType": "infoblock",
            "displayLabel": null,
            "content": "Please select License acquisition and upgrade support topic in previous screen.",
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
            "id": "groupOrUserAssignment",
            "visibility": purchaseOrUpgrade!=yes,
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Are you assigning license directly to users or assigning license to a group",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Direct",
                    "value": "direct"
                },
                {
                    "text": "Group",
                    "value": "group"
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
            "id": "groupName",
            "visibility": "groupOrUserAssignment!=user",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "What is name or id of the group having issue?",
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
            "id": "onpremOrCloud",
            "visibility": groupOrUserAssignment!=user,
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Is the group synced from on-prem active directory?",
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
            "id": "onpremOrCloud",
            "visibility": groupOrUserAssignment!=user,
            "order": 6,
            "controlType": "dropdown",
            "displayLabel": "What is the membership Type of the group?",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Assigned",
                    "value": "assigned"
                },
                {
                    "text": "Dynamic",
                    "value": "dynamic"
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
            "id": "userUPN",
            "visibility": null,
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "What is UPN of the user having issue?",
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
        },
        {
            "id": "userCID",
            "visibility": null,
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "If you have the correlation if of the failure please provide",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "hints": null,
            "required": no,
            "maxLength": 0,
            "useAsAdditionalDetails": true,
            "numberOfLines": 0
        }
    ],
    "$schema": "SelfHelpContent"
}
---