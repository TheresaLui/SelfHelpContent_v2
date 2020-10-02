<properties
    pageTitle="setup-and-config"
    description="Problem with setup"
    authors="jbeman"
    ms.author="jbeman"
    selfHelpType="problemScopingQuestions"
    supportTopicIds=""
    productPesIds="16918"
    cloudEnvironments="public, fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="problemscopingques-coresetup"
	ownershipId="AzureIot_Mobility"
/>

# Problem with Setup

---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Problem with Setup",
    "fileAttachmentHint": null,
    "formElements": [
        {
            "id": "problem_start_time",
            "visibility": null,
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem occur?",
            "required": true
        },
        {
            "id": "problem_region",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Which region is your VM and/or cluster located?",
            "watermarkText": "Azure Region",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Please describe your problem",
            "watermarkText": "Problem description",
            "useAsAdditionalDetails": true,
            "required": true
        },
        {
            "id": "subscription_user",
            "visibility": null,
            "order": 4,
            "controlType": "radiobuttongroup",
            "displayLabel": "Is your IT department managing your subscription or are you using a personal one?",
                "radioButtonOptions": [{
                        "value": "IT",
                        "text": "IT managed"
                    },
                    {
                        "value": "Personal",
                        "text": "Personal"
                    }
                ],
            "required": true
        },
        {
            "id": "deployment_type",
            "order": 5,
            "controlType": "multiselectdropdown",
            "displayLabel": "What type of deployment are you working on?",
            "dropdownOptions": [{
                    "value": "DevSetup",
                    "text": "DevSetup (Partner Kit)"
                }, {
                    "value": "EasyButton",
                    "text": "EasyButton"
                }, {
                    "value": "Test_Cluster",
                    "text": "Test Cluster"
                },{
                    "value": "Production",
                    "text": "Production"
                },  {
                    "text": "I don't know",
                    "value": "dont_know_answer"
                }
            ],
            "required": false
        },
        {
            "id": "version",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "What version of MCVP core are you attempting to deploy?",
            "required": true
        },
        {
            "id": "permissions_subscription",
            "order": 7,
            "controlType": "dropdown",
            "displayLabel": "What highest permission do you have for your subscription?",
            "dropdownOptions": [{
                    "value": "Administator",
                    "text": "Administator"
                }, {
                    "value": "Owner",
                    "text": "Owner"
                }, {
                    "value": "Contributor",
                    "text": "Contributor"
                },{
                    "value": "Reader",
                    "text": "Reader"
                },  {
                    "text": "I don't know",
                    "value": "dont_know_answer"
                }
            ],
            "required": true
        },
        {
            "id": "permissions",
            "order": 8,
            "controlType": "multiselectdropdown",
            "displayLabel": "What permissions do you have in Azure Active Directory for your subscription?",
            "dropdownOptions": [{
                    "value": "Global Administrator",
                    "text": "Global Administrator"
                }, {
                    "value": "Application Developer",
                    "text": "Application Developer"
                }, {
                    "value": "User Administrator",
                    "text": "User Administrator"
                },{
                    "value": "Other",
                    "text": "Other"
                },  {
                    "text": "I don't know",
                    "value": "dont_know_answer"
                }
            ],
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---
