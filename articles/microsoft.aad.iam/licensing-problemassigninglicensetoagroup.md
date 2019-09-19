<properties
    pageTitle="Problem assigning licenses to a group"
    description="problemassigninglicensetoagroup"
    authors="chpate"
    ms.author="chpate"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32615386"
    productPesIds="16578,16575,16578"
    cloudEnvironments="public"
    schemaVersion="1"
    articleId="23c1cf4d-6fdd-475b-ba06-87595b53195b"
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
            "id": "tenantSubscription",
            "visibility": null,
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Does the tenant have a subscription for a premium Azure AD product?",
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
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "dynamicDropdownOptions": null,
            "required": true,
            "maxLength": 0,
            "numberOfLines": 0
        },
        {
            "id": "licenseRequirement",
            "visibility": "tenantSubscription!=yes",
            "order": 4,
            "controlType": "infoblock",
            "displayLabel": null,
            "content": "<a href='https://docs.microsoft.com/azure/active-directory/active-directory-licensing-whatis-azure-portal'>Assigning licenses to groups is currently in Public Preview and requires an active subscription for one of the Azure AD products, such as: Azure AD Basic, Azure AD Premium, or Enterprise Mobility + Security. You can see the list of your subscriptions under Azure Active Directory--Licenses--All Products. Click here to read more about the preview and the license requirement to use this feature.</a>",
            "watermarkText": null,
            "infoBalloonText": null,
            "dynamicDropdownOptions": null,
            "required": false,
            "maxLength": 0,
            "numberOfLines": 0
        },
        {
            "id": "whereProblem",
            "visibility": null,
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "What environment are you using to assign a license to a group?",
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
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "dynamicDropdownOptions": null,
            "required": true,
            "maxLength": 0,
            "numberOfLines": 0
        },
        {
            "id": "portalAvailability",
            "visibility": "whereProblem!=azurePortal",
            "order": 6,
            "controlType": "infoblock",
            "displayLabel": null,
            "content": "<a href='https://docs.microsoft.com/azure/active-directory/active-directory-licensing-group-assignment-azure-portal'>Assigning licenses to groups is only available through the Azure portal. Open the group in the portal, go to the Licenses tab to view or modify a license on a group. Click here to find out more.</a>",
            "watermarkText": null,
            "infoBalloonText": null,
            "dynamicDropdownOptions": null,
            "required": false,
            "maxLength": 0,
            "numberOfLines": 0
        },
        {
            "id": "groupId",
            "visibility": null,
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the Object ID of the group you are having problems with?",
            "content": null,
            "watermarkText": "The Object ID can be found by opening the group in the portal, in the Overview tab in the Essentials box on the very top.",
            "infoBalloonText": null,
            "dynamicDropdownOptions": null,
            "required": false,
            "maxLength": 0,
            "numberOfLines": 2
        },
        {
            "id": "symptoms",
            "visibility": null,
            "order": 8,
            "controlType": "multilinetextbox",
            "displayLabel": "What are the symptoms of the problem?",
            "content": null,
            "watermarkText": "Tell us what you are trying to accomplish and what is not working.",
            "infoBalloonText": null,
            "dynamicDropdownOptions": null,
            "required": false,
            "maxLength": 0,
            "numberOfLines": 4
        },
        {
            "id": "problem_start_time",
            "visibility": null,
            "order": 9,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dynamicDropdownOptions": null,
            "required": false,
            "maxLength": 0,
            "numberOfLines": 0
        },
        {
            "id": "problem_description",
            "visibility": null,
            "order": 10,
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