<properties
    pageTitle="setup-and-config"
    description="Problem with setup"
    authors="jbeman"
    ms.author="jbeman"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32725767"
    productPesIds="16918"
    cloudEnvironments="public"
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
            "id": "start_time",
            "visibility": null,
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem occur?",
            "required": true
        },
        {
            "id": "subscription_user",
            "visibility": null,
            "order": 2,
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
            "id": "region_location",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Which region is your VM and/or cluster located?",
            "required": false,
            "useAsAdditionalDetails": true,
            "hints": [{
                    "text": "Provide the region name for your setup"
                }, {
                    "text": "https://azure.microsoft.com/en-us/global-infrastructure/geographies/"
                }
            ],
            "required": true
        },
        {
            "id": "deployment_type",
            "order": 4,
            "controlType": "multiselectdropdown",
            "displayLabel": "What type of deployment are you working on?",
            "dropdownOptions": [{
                    "value": "DevSetup (Partner Kit)",
                    "text": "DevSetup"
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
                    "value": "dont_know"
                }
            ],
            "required": true
        },
        {
            "id": "version",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "What version of MCVP core are you attempting to deploy?",
            "required": false,
            "useAsAdditionalDetails": true,
            "hints": [{
                    "text": "The Partner Kit version is found in a text file under cloud/core/version.txt"
                }, {
                    "text": "https://dev.azure.com/mcvp-prod/Partner%20Kits/_git/mcvp-pkit?path=%2Fcloud%2FCore%2Fversion.txt"
                }
            ],
            "required": true
        },
        {
            "id": "permissions_subscription",
            "order": 6,
            "controlType": "multiselectdropdown",
            "displayLabel": "What permissions do you have for your subscription?",
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
                    "value": "dont_know"
                }
            ],
            "required": true
        },
        {
            "id": "permissions_aad",
            "order": 7,
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
                    "value": "dont_know"
                }
            ],
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
