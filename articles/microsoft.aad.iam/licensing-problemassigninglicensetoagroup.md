<properties
    pageTitle="Problem assigning licenses to a group"
    description="problemassigninglicensetoagroup"
    authors="chpate"
    ms.author="chpate"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32615386"
    productPesIds="16575,16578"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    schemaVersion="1"
    articleId="23c1cf4d-6fdd-475b-ba06-87595b53195b"
    	ownershipId="AzureIdentity_AppDevelopmentAndRegistration"
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
            "id": "groupOrUserAssignment",
            "visibility": "null",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "License assignment",
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
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Name or id of the group",
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
            "visibility": "groupOrUserAssignment==group",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Group synced from on-prem active directory",
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
            "id": "groupMembershipType",
            "visibility": "groupOrUserAssignment==group",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Membership Type of the group",
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
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "UPN of the user",
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
            "id": "userCID",
            "visibility": null,
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "Correlation of the failure",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "required": false,
            "maxLength": 0,
            "numberOfLines": 2
        },
        {
            "id": "problem_start_time",
            "visibility": null,
            "order": 7,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dynamicDropdownOptions": null,
            "required": true,
            "maxLength": 0,
            "numberOfLines": 0
        },
        {
            "id": "problem_description",
            "visibility": null,
            "order": 8,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional details",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dynamicDropdownOptions": null,
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": true,
            "numberOfLines": 0
        }
    ],
    "$schema": "SelfHelpContent"
}
---
