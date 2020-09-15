<properties
    pageTitle="vehicle-provisioning"
    description="Problem with vehicle or device provisioning"
    authors="jbeman"
    ms.author="jbeman"
    selfHelpType="problemScopingQuestions"
    supportTopicIds=""
    productPesIds="16918"
    cloudEnvironments="public"
    schemaVersion="1"
    articleId="problemscopingques-coreprovisioning"
	ownershipId="AzureIot_Mobility"
/>

# Problem with vehicle or device provisioning

---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Problem with vehicle or device provisioning",
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
            "id": "problem_region",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Which region is your VM and/or cluster located?",
            "required": true
        },
        {
            "id": "deployment_type",
            "order": 3,
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
                    "value": "dont_know_answer"
                }
            ],
            "required": true
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
