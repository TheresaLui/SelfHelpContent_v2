<properties
         pageTitle="Scoping questions for MARS backup failure"
         description="Scoping questions for MARS backup failure"
         authors="srinathvasireddy"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32553275"
         productPesIds="15207"
         cloudEnvironments="public"
         schemaVersion="1"
/>
# Questions MARS backup failure
---
{
         "resourceRequired": true,
         "title": "MARS backup failure",
         "fileAttachmentHint": "",
         "formElements": [{
			 "id": "os_version",
			 "order": 1,
			 "controlType": "textbox",
			 "displayLabel": "What is the OS version of the impacted system?",
			 "watermarkText": "Provide the OS version of the impacted system",
			 "required": true
		 }, {
                         "id": "lastbackup_successful",
                         "order": 2,
                         "controlType": "datetimepicker",
			 "displayLabel": "When did the last backup successfully completed?",
			 "required": false
		 }, {
			 "id": "Select_ErrorMessage",
			 "order": 3,
			 "controlType": "dropdown",
			 "displayLabel": "Select the error message that you are seeing?",
			 "watermarkText": "Select",
			 "dropdownOptions": [{
				           "value": "Invalid vault credentials provided. The file is either corrupted...",
				           "text": "Invalid vault credentials provided. The file is either corrupted..."
				}, {
					   "value": "The Microsoft Azure Recovery Service Agent was unable to connect to Microsoft Azure Backup",
				           "text": "The Microsoft Azure Recovery Service Agent was unable to connect to Microsoft Azure Backup"
				}, {
					   "value": "(407) Proxy Authentication Required",
					   "text": "(407) Proxy Authentication Required"
				}, {
					   "value": "The encryption passphrase stored on this computer is not correctly configured",
					   "text": "The encryption passphrase stored on this computer is not correctly configured"
				   }
			       ],
				"required": true
	   }, {
			"id": "Basic_troubleshooting_multiselect",
			"order": 4,
			"controlType": "multiselectdropdown",
			"displayLabel": "Select the troubleshooting steps you have completed:",
			"dropdownOptions": [{
					   "value": "MARS agent is latest",
					   "text": "MARS agent is latest"
				}, {
					   "value": "CBEngine Service is running",
					   "text": "CBEngine Service is running"
				}, {
					   "value": "Machine has Internet connectivity",
					   "text": "Machine has Internet connectivity"
				}, {
					   "value": "5-10% free volume space is available on scratch folder location",
					   "text": "5-10% free volume space is available on scratch folder location"
			        }, {
					   "value": "Antivirus software is running on the machine",
					   "text": "Antivirus software is running on the machine"
				}, {
					   "value": "Using Proxy server",
					   "text": "Using Proxy server"
				  }
			    ],
				"required": true
		}, {
			"id": "problem_start_date",
			"order": 5,
			"controlType": "datetimepicker",
			"displayLabel": "When did the problem begin?",
			"required": false
		}, {
			"id": "learn_more_text",
			"order": 6,
			"controlType": "infoblock",
			"content": "Microsoft can provide a solution to your problem faster if you can attach the latest CBEngine Logs. You can find this from C:\Program Files\Microsoft Azure Recovery Services Agent\Temp"
		}
	]
}
---
