<properties
    pageTitle="Azure Media Player common questions"
    description="Azure Media Player common questions"
    authors="johndeu"
    ms.author="johndeu"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32632081, 32632086, 32632099, 32632111, 32632077, 32729550"
    productPesIds="14885"
    articleId="problemscopingques-amp-common"
    cloudEnvironments="public, fairfax, usnat, ussec"
    schemaVersion="1"
	ownershipId="StorageMediaEdge_Media"
/>
# Azure Media Player common questions for support
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Azure Media Player common questions for support",
    "fileAttachmentHint": "Please follow the instructions in the Player documentation to enable verbose logging and attach log files here. If the issue you are reporting is 'visible' or decoder related, please upload a short video of the problem.",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the issue begin?",
            "required": true
        },
        {
            "id": "amp_browser",
            "order": 2,
            "controlType": "multiselectdropdown",
            "infoBalloonText": "See the matrix of <a href='http://amp.azure.net/libs/amp/latest/docs/index.html#compatibility-matrix'>supported browsers and operating systems</a>",
            "displayLabel": "Please select the browsers impacted by the issue.",
            "watermarkText": "Select the browsers impacted",
            "dropdownOptions": [
                {
                    "value": "Microsoft Edge EdgeHTML",
                    "text": "Microsoft Edge (EdgeHTML 2014-2019)"
                },
                {
                    "value": "Microsoft Edge Chromium",
                    "text": "Microsoft Edge (Chromium 2019-present)"
                },
                {
                    "value": "Microsoft IE 11",
                    "text": "Microsoft IE 11"
                },
                {
                    "value": "Google Chrome 37+",
                    "text": "Google Chrome 37 or higher"
                },
                {
                    "value": "Mozilla Firefox 42+",
                    "text": "Mozilla Firefox 42 or higher"
                },
                {
                    "value": "Apple Safari 8+",
                    "text": "Apple Safari 8 or higher"
                },
                {
                    "value": "Apple Safari 6-7",
                    "text": "Apple Safari 6-7"
                },
                {
                    "value": "Other",
                    "text": "Other (unsupported)"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't Know"
                }
            ],
            "required": true
        },
        {
            "id": "amp_os",
            "order": 3,
            "controlType": "multiselectdropdown",
            "displayLabel": "Select the operating systems where the issue occurred.",
            "watermarkText": "Choose multiple options",
            "dropdownOptions": [
                {
                    "value": "Windows 10",
                    "text": "Windows 10 "
                },
                {
                    "value": "Windows 8.1",
                    "text": "Windows 8.1"
                },
                {
                    "value": "Windows 7",
                    "text": "Windows 7"
                },
                {
                    "value": "Windows Vista",
                    "text": "Windows Vista"
                },
                {
                    "value": "Apple iOS 12",
                    "text": "Apple iOS 12 or higher"
                },
                {
                    "value": "Apple iOS 11",
                    "text": "Apple iOS 11"
                },
                {
                    "value": "Apple iOS 10",
                    "text": "Apple iOS 10"
                },
                {
                    "value": "Apple OS X Yosemite+",
                    "text": "Apple OS X Yosemite or higher"
                },
                {
                    "value": "Apple OS X Mountain Lion",
                    "text": "Apple OS X Mountain Lion"
                },
                {
                    "value": "Android 5.0+",
                    "text": "Android 5.0 or higher"
                },
                {
                    "value": "Android 4.4.4",
                    "text": "Android 4.4.4 up to 5.0"
                },
                {
                    "value": "Android 4.0",
                    "text": "Android 4.0"
                },
                {
                    "value": "XBOX One",
                    "text": "XBOX One"
                },
                {
                    "value": "Other",
                    "text": "Other"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't Know"
                }
            ],
            "required": true
        },
        {
            "id": "amp_version",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Which version of Azure Media Player?",
            "infoBalloonText": "See list of versions and release notes <a href='http://amp.azure.net/libs/amp/latest/docs/changelog.html'>here</a> in the documentation.",
            "dropdownOptions": [
                {
                    "value": "2.2.4+",
                    "text": "2.2.4 or higher"
                },
                {
                    "value": "2.2.3",
                    "text": "2.2.3"
                },
                {
                    "value": "2.2.2",
                    "text": "2.2.2"
                },
                {
                    "value": "2.2.1",
                    "text": "2.2.1"
                },
                {
                    "value": "2.2.0",
                    "text": "2.2.0"
                },
                {
                    "value": "2.1.9",
                    "text": "2.1.9"
                },
                {
                    "value": "2.1.8",
                    "text": "2.1.8"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't Know"
                }
            ],
            "required": false
        },
        {
            "id": "amp_error_code",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the error code provided by the player?",
            "watermarkText": "Please provide any error codes displayed in the Player.",
            "infoBalloonText": "See list of error codes and how to find them  <a href='http://amp.azure.net/libs/amp/latest/docs/index.html#error-codes'>here</a> in the documentation.",
            "required": false
        },
        {
            "id": "amp_drm_in_use",
            "order": 6,
            "controlType": "multiselectdropdown",
            "displayLabel": "Are you using DRM or AES encryption?",
            "watermarkText": "Please select the DRM or encryption in use that is related to this error report",
            "infoBalloonText": "See details on DRM compatibility <a href='http://amp.azure.net/libs/amp/latest/docs/index.html#compatibility-matrix'>here</a> in the documentation.",
            "dropdownOptions": [
                {
                    "value": "not_used",
                    "text": "Not used"
                },
                {
                    "value": "PlayReady",
                    "text": "PlayReady"
                },
                {
                    "value": "FairPlay",
                    "text": "FairPlay"
                },
                {
                    "value": "Widevine",
                    "text": "Widevine"
                },
                {
                    "value": "AES clear key",
                    "text": "AES clear key"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't Know"
                }
            ],
            "required": false
        },
        {
            "id": "amp_drm_issue",
            "order": 7,
            "controlType": "multilinetextbox",
            "displayLabel": "What DRM or encryption settings are you using?",
            "visibility": "amp_drm_in_use != dont_know_answer || amp_drm_in_use != not_used",
            "watermarkText": "Please provide details on the DRM configuration and settings used. Provide an example of the Policy settings used.",
            "infoBalloonText": "See details on DRM compatibility <a href='http://amp.azure.net/libs/amp/latest/docs/index.html#compatibility-matrix'>here</a> in the documentation.",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 8,
            "controlType": "multilinetextbox",
            "displayLabel": "Scenario details",
            "watermarkText": "Provide additional details about the problem and scenario that you ran into with the player",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Provide details about the scenario and issues that you ran into with the player. Be sure to note if this worked previously and suddenly stopped working, and if possible provide a URL to a hosted test player that demonstrates or reproduces your issue (example - use stackblitz.com to reproduce the issue and include link here)"
                }
            ]
        },
        {
            "id": "amp_repro_steps",
            "order": 9,
            "controlType": "multilinetextbox",
            "displayLabel": "Repro steps or links to player showing issue",
            "watermarkText": "Please provide repro steps and a link to a hosted version of the player (on a web site like jsfiddle.net, github.com or stackblitz.com for example) that shows the reported behavior",
            "required": false,
            "useAsAdditionalDetails": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---
