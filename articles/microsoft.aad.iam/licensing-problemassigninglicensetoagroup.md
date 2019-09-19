<properties
    pageTitle="Problem assigning licenses to a group"
    description="problemassigninglicensetoagroup"
    authors="chpate"
    ms.author="chpate"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32570958,32615386"
    productPesIds="14785,16578,16575,16578"
    cloudEnvironments="public"
    schemaVersion="1"
    articleId="licensing-problemassigninglicensetoagroup"
    />

# Problem assigning licenses to a group

---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "Problem assigning licenses to a group",
    "fileAttachmentHint": null,
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "purchaseOrUpgrade",
            "visibility": null,
            "order": 3,
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
                },
                ,
                {
                    "value": "dont_know_answer",
                    "text": "Not sure"
                }
            ],
            "dynamicDropdownOptions": null,
            "required": true,
            "maxLength": 0,
            "numberOfLines": 0
        },
        {
            "id": "purchaseOrUpgradeSelected",
            "visibility": "purchaseOrUpgrade==yes",
            "order": 4,
            "controlType": "infoblock",
            "displayLabel": null,
            "content": "Please select License acquisition and upgrade support topic in previous screen.",
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "required": false,
            "maxLength": 0,
            "numberOfLines": 0
        },
        {
            "id": "groupOrUserAssignment",
            "visibility": "purchaseOrUpgrade==no",
            "order": 5,
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
                },
                {
                    "value": "dont_know_answer",
                    "text": "Not sure"
                }
            ],
            "dynamicDropdownOptions": null,
            "required": true,
            "maxLength": 0,
            "numberOfLines": 0
        },
        {
            "id": "groupName",
            "visibility": "groupOrUserAssignment==group",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "What is name or id of the group having issue?",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "required": true,
            "maxLength": 0,
            "numberOfLines": 2
        },
        {
            "id": "onpremOrCloud",
            "visibility": groupOrUserAssignment==group,
            "order": 7,
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
            "required": true,
            "maxLength": 0,
            "numberOfLines": 0
        },
        {
            "id": "groupMembershipType",
            "visibility": groupOrUserAssignment==group,
            "order": 8,
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
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't know"
                }
            ],
            "dynamicDropdownOptions": null,
            "required": true,
            "maxLength": 0,
            "numberOfLines": 0
        },
        {
            "id": "userUPN",
            "visibility": null,
            "order": 9,
            "controlType": "multilinetextbox",
            "displayLabel": "What is UPN of the user having issue?",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": true,
            "numberOfLines": 0
        },
        {
            "id": "userCID",
            "visibility": null,
            "order": 9,
            "controlType": "multilinetextbox",
            "displayLabel": "If you have the correlation if of the failure please provide",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "required": no,
            "maxLength": 0,
            "useAsAdditionalDetails": true,
            "numberOfLines": 0
        }
    ],
    "$schema": "SelfHelpContent"
}
---