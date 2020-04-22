<properties pageTitle="Problem with User sign-in WHFB" 
	 description="usersigninwhfbscopingquestions" 
	 authors="anupnadigm" 
	 selfHelpType="problemScopingQuestions" 
	 supportTopicIds="32596873" 
	 productPesIds="14785,16579" 
	 cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec" 
	 schemaVersion="1"
    articleId="7262a9ca-3a86-4f67-9acf-b702dd50f0e9"
	ownershipId="AzureIdentity_MultiFactorAuthentication"
/> 
#  Problem with User sign-in WHFB
---
{
    "resourceRequired": false,
    "title": "Problem with User sign-in WHFB",
    "fileAttachmentHint": null,
    "formElements": [
        {
            "id": "whfbPrb",
            "visibility": null,
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Tell us about your problem?",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "I haven't setup WHfB and need help getting started.",
                    "value": "whfbPrbsetup"
                },
                {
                    "text": "I've set up WHfB but isn't working.",
                    "value": "whfbPrbnotworking"
                },
                {
                    "text": "Other, don't know or not applicable",
                    "value": "ptother"
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
            "id": "whfbsetupgeneralguide",
            "visibility": "whfbsetup==whfbsetupgeneral",
            "order": 2,
            "controlType": "infoblock",
            "displayLabel": null,
            "content": "<a href='https://aka.ms/whfbplan'>Click here to get started with the WHfB Planning Guide.</a>",
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
            "id": "whfbsetup",
            "visibility": "whfbPrb==whfbPrbsetup",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "What type of setup help do you need?",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "I need general help getting started.",
                    "value": "whfbsetupgeneral"
                },
                {
                    "text": "I have specific questions not covered in documentation.",
                    "value": "whfbsetupspecific"
                },
                {
                    "text": "Other, don't know or not applicable",
                    "value": "whfbsetupother"
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
            "id": "whfbsetupspecificfaq",
            "visibility": "whfbsetup==whfbsetupspecific",
            "order": 4,
            "controlType": "infoblock",
            "displayLabel": null,
            "content": "<a href='https://docs.microsoft.com/windows/security/identity-protection/hello-for-business/hello-identity-verification#frequently-asked-questions'>Click here to make sure your question isn't already answered in our FAQ.</a>",
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
            "id": "whfbsetupspecificdetal",
            "visibility": "whfbsetup==whfbsetupspecific",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Tell us what question(s) you weren't able to find answers to:",
            "content": null,
            "watermarkText": "I can't find information on how to ....",
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "hints": [],
            "required": true,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 4
        },
        {
            "id": "whfbnotworkingcommon",
            "visibility": "whfbPrb==whfbPrbnotworking",
            "order": 6,
            "controlType": "dropdown",
            "displayLabel": "Select your issue from these common problems?",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "I do not get prompted to register for a PIN",
                    "value": "nopinprompt"
                },
                {
                    "text": "I experience failures during PIN enrollment",
                    "value": "pinenrollfail"
                },
                {
                    "text": "My biometrics or PIN are not working for Sign-in",
                    "value": "biometric"
                },
                {
                    "text": "Other, don't know or not applicable",
                    "value": "whfbfailother"
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
            "id": "whfbdeployment",
            "visibility": "whfbPrb==whfbPrbnotworking",
            "order": 7,
            "controlType": "dropdown",
            "displayLabel": "From the problem device, I plan to access resources that are located:",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Cloud ONLY",
                    "value": "whfbdetaildeploymentcloud"
                },
                {
                    "text": "Hybrid (Cloud AND On-premises)",
                    "value": "whfbdetaildeploymenthybrid"
                },
                {
                    "text": "On-Premises ONLY",
                    "value": "whfbdetaildeploymentonprem"
                },
                {
                    "text": "Other, don't know or not applicable",
                    "value": "whfbdetaildeploymentunknown"
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
            "id": "whfbdetailhybridtrust",
            "visibility": "whfbdeployment==whfbdetaildeploymenthybrid",
            "order": 8,
            "controlType": "dropdown",
            "displayLabel": "Which WHfB trust type are you using?",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Key Trust (group policy managed)",
                    "value": "whfbdetailhybridtrustkeygp"
                },
                {
                    "text": "Key Trust (MDM managed)",
                    "value": "whfbdetailhybridtrustkeymdm"
                },
                {
                    "text": "Certificate Trust (MDM managed)",
                    "value": "whfbdetailhybridtrustcertmdm"
                },
                {
                    "text": "Certificate Trust (mixed managed)",
                    "value": "whfbdetailhybridtrustcertmixed"
                },
                {
                    "text": "Other, don't know or not applicable",
                    "value": "whfbdetailhybridtrustunknown"
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
            "id": "whfbdetailhybridmfa",
            "visibility": "whfbdeployment==whfbdetaildeploymenthybrid",
            "order": 9,
            "controlType": "dropdown",
            "displayLabel": "Which MFA solution are you using?",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Azure MFA",
                    "value": "whfbdetailhybridmfaazuremfa"
                },
                {
                    "text": "AD FS with Azure MFA Adapter",
                    "value": "whfbdetailhybridmfaadfsmfaserver"
                },
                {
                    "text": "AD FS with Azure MFA Server",
                    "value": "whfbdetailhybridmfaadfsmfaadapter"
                },
                {
                    "text": "AD FS with 3rd Party MFA Adapter",
                    "value": "whfbdetailhybridmfaadfs3rdpartyadapter"
                },
                {
                    "text": "Other, don't know or not applicable",
                    "value": "whfbdetailhybridmfaunknown"
                }
            ],
            "dynamicDropdownOptions": null,
            "hints": [],
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "whfbdetailonpremtrust",
            "visibility": "whfbdeployment==whfbdetaildeploymentonprem",
            "order": 10,
            "controlType": "dropdown",
            "displayLabel": "Which WHfB trust type are you using?",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Key Trust (group policy managed)",
                    "value": "whfbdetailonpremtrustkeygp"
                },
                {
                    "text": "Certificate Trust (group policy managed)",
                    "value": "whfbdetailonpremtrustcertgp"
                },
                {
                    "text": "Other, don't know or not applicable",
                    "value": "whfbdetailonpremtrustunknown"
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
            "id": "whfbdetailonpremmfa",
            "visibility": "whfbdeployment==whfbdetaildeploymentonprem",
            "order": 11,
            "controlType": "dropdown",
            "displayLabel": "Which MFA solution are you using?",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "AD FS with Azure MFA Server",
                    "value": "whfbdetailonpremmfaadfsmfaserver"
                },
                {
                    "text": "AD FS with 3rd Party MFA Adapter",
                    "value": "whfbdetailonpremmfaadfs3rdparty"
                },
                {
                    "text": "Other, don't know or not applicable",
                    "value": "whfbdetailonpremmfaunknown"
                }
            ],
            "dynamicDropdownOptions": null,
            "hints": [],
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "whfbdetailcloudtrust",
            "visibility": "whfbdeployment==whfbdetaildeploymentcloud",
            "order": 12,
            "controlType": "dropdown",
            "displayLabel": "Which WHfB trust type are you using?",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Key Trust (MDM managed)",
                    "value": "whfbdetailcloudtrustkeymdm"
                },
                {
                    "text": "Other, don't know or not applicable",
                    "value": "whfbdetailcloudtrustunknown"
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
            "id": "whfbdetailcloudmfa",
            "visibility": "whfbdeployment==whfbdetaildeploymentonprem",
            "order": 13,
            "controlType": "dropdown",
            "displayLabel": "Which MFA solution are you using?",
            "content": null,
            "watermarkText": null,
            "infoBalloonText": null,
            "dropdownOptions": [
                {
                    "text": "Azure MFA",
                    "value": "whfbdetailcloudmfaazuremfa"
                },
                {
                    "text": "Other, don't know or not applicable",
                    "value": "whfbdetailcloudmfaunknown"
                }
            ],
            "dynamicDropdownOptions": null,
            "hints": [],
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "whfbdetailwin10Ver",
            "visibility": "whfbPrb==whfbPrbnotworking",
            "order": 14,
            "controlType": "multilinetextbox",
            "displayLabel": "Windows 10 OS Version/Build info (Press Windows+R and type WinVer):",
            "content": null,
            "watermarkText": "Ex. Version 1709 OS build 16299.192",
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "hints": [],
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 1
        },
        {
            "id": "problem_description",
            "visibility": null,
            "order": 15,
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
        },
        {
            "id": "problem_start_time",
            "order": 16,
            "controlType": "datetimepicker",
            "displayLabel": "Problem start time",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---