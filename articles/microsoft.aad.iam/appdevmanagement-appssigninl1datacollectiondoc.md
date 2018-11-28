<properties
    pageTitle="Active Directory application sign in L1 issue"
    description="appssigninl1datacollectiondoc"
    authors="anupnadigm"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32570955,32596851,32596848,32596856,32596837,32268132,32570275,32570259,32570274,32596862,32615379,32615388,32615397,32615424,32596867,32615381,32615390,32615398,32447987,32596842,32596872,32615399,32615515,32615516,32615400,32615519"
    productPesIds="16575,16579"
    cloudEnvironments="public"
    schemaVersion="1"
    articleId="f394c94f-4550-4d6c-87ec-84a57305bfcd"
    />

# Active Directory application sign in L1 issue

---
{
    "resourceRequired": false,
    "title": "Active Directory application sign in L1 issue",
    "fileAttachmentHint": null,
    "formElements": [
        {
            "id": "VerboseTracing",
            "visibility": null,
            "order": 1,
            "controlType": "infoblock",
            "displayLabel": null,
            "content": "Before requesting support, Microsoft suggests you enable advanced diagnostics that will gather more information about your problem.",
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
            "id": "enableVerboseTracing1",
            "visibility": null,
            "order": 2,
            "controlType": "infoblock",
            "displayLabel": null,
            "content": "To enable advance diagnosis:",
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
            "id": "enableVerboseTracing2",
            "visibility": null,
            "order": 3,
            "controlType": "infoblock",
            "displayLabel": null,
            "content": "Open a new browser tab and paste https://login.microsoftonline.com/common/debugmode/enable?user={username} (replace {username} with the upn of the user in question; eg: user=johndoe@contoso.com) and then try to reproduce the error.",
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
            "id": "hasErrorData",
            "visibility": null,
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Do you have a correlation ID and Timestamp for an error related to this problem?",
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
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 0
        },
        {
            "id": "getCorrelationId",
            "visibility": "hasErrorData==no",
            "order": 5,
            "controlType": "infoblock",
            "displayLabel": null,
            "content": "Microsoft can provide a solution to your problem faster if you can get a correlation ID and Timestamp for this problem, reproduce the error by signing into the app with your own account.",
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
            "id": "correlationId",
            "visibility": "hasErrorData==yes",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "Correlation ID from Error message:",
            "content": null,
            "watermarkText": "Copy the correlation ID from the error message and paste it here",
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
            "id": "timestamp",
            "visibility": "hasErrorData==yes || hasErrorData==no",
            "order": 7,
            "controlType": "textbox",
            "displayLabel": "Timestamp from Error message:",
            "content": null,
            "watermarkText": "Copy the timestamp from the error message and paste it here",
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
            "id": "appNameOrId",
            "visibility": "hasErrorData==no",
            "order": 8,
            "controlType": "multilinetextbox",
            "displayLabel": "What is the Application name or Application ID experiencing this problem?",
            "content": null,
            "watermarkText": "Application ID is in the Properties section in the Azure AD configuration for the application",
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "hints": [],
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": false,
            "numberOfLines": 2
        },
        {
            "id": "userNameOrId",
            "visibility": "hasErrorData==no",
            "order": 9,
            "controlType": "textbox",
            "displayLabel": "Which user is experiencing this problem?",
            "content": null,
            "watermarkText": "Enter user upn or Object ID of the user in Azure Active Directory",
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
            "id": "problem_description",
            "visibility": null,
            "order": 10,
            "controlType": "multilinetextbox",
            "displayLabel": "If you received an error, please provide the error message details:",
            "content": null,
            "watermarkText": "AADSTSXXXXX: error message, Error message from the application, etc... ",
            "infoBalloonText": null,
            "dropdownOptions": null,
            "dynamicDropdownOptions": null,
            "hints": null,
            "required": false,
            "maxLength": 0,
            "useAsAdditionalDetails": true,
            "numberOfLines": 3
        },
        {
            "id": "problem_start_time",
            "order": 11,
            "controlType": "datetimepicker",
            "displayLabel": "Problem start time",
            "required": true
        }
    ]
}
---