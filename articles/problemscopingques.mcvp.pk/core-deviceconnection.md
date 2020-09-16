<properties
    pageTitle="device-connection"
    description="Problem with the device connection"
    authors="jbeman"
    ms.author="jbeman"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32725758"
    productPesIds="16918"
    cloudEnvironments="public"
    schemaVersion="1"
    articleId="problemscopingques-coredeviceconnection"
	ownershipId="AzureIot_Mobility"
/>

# Problem with the device connection

---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Problem with the device connection",
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
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "What version of MCVP core are you attempting to deploy?",
            "required": true
        },
        {
            "id": "permissions_subscription",
            "order": 5,
            "controlType": "radiobuttongroup",
            "displayLabel": "Is your service fabric healthy and showing green for the MCVP apps and services?",
            "radioButtonOptions": [{
                    "value": "Yes",
                    "text": "Yes"
                }, {
                    "value": "No",
                    "text": "No"
                }
            ],
            "required": true
        },
        {
            "id": "permissions_aad",
            "order": 6,
            "controlType": "radiobuttongroup",
            "displayLabel": "Did you successfully install the PFX file onto your machine?",
           "radioButtonOptions": [{
                    "value": "Yes",
                    "text": "Yes"
                }, {
                    "value": "No",
                    "text": "No"
                }
            ],
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
