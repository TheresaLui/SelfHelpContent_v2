<properties
	pageTitle="V2A Replication not progressing"
	description="V2A Replication not progressing"
	authors="srinathv"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32536441"
	productPesIds="15207"
	cloudEnvironments="public"
	schemaVersion="1"
/>
# V2A Replication not progressing
---
{
	"resourceRequired": false,
	"title": "V2A Replication not progressing",
	"fileAttachmentHint": "",
	"formElements": [{
			"id": "learn_more_text",
			"order": 1,
			"controlType": "infoblock",
			"content": "<b>Review the resources listed as they may help you solve your issue without needing to open a support case</b>
				<ul><li>Follow steps listed in this<a href='https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-protection-troubleshoot'> article</a> to resolve common Replication issues.</li>
         <li> Run the<a href= 'https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-deployment-planner-run'> Deployment planner</a> and review recommendations for<a href= 'https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-deployment-planner-analyze-report#recommendations-with-available-bandwidth-as-input'> network</a> and <a href= 'https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-deployment-planner-analyze-report#vm-storage-placement'> storage </a>. Check if you need to adjust the bandwidth and throttling as listed in this<a href= 'https://docs.microsoft.com/azure/site-recovery/site-recovery-plan-capacity-vmware#control-network-bandwidth'> article.</a></li></ul>"
		},  {
			"id": "problem_os_version",
			"order": 2,
			"controlType": "textbox",
			"displayLabel": "What is the Operating System version (and kernel version for Linux) of the VM that you are trying to protect?",
			"watermarkText": "Ex: Windows Server 2016, Ubuntu 16.04 LTS server kernel 4.10.0-14-generic to 4.10.0-32-generic",
			"useAsAdditionalDetails": false,
			"required": true
		}, {
			"id": "learn_more_text_1",
			"order": 3,
			"controlType": "infoblock",
			"content": "To find the list of supported Operating System <a href='https://docs.microsoft.com/azure/site-recovery/support-matrix-vmware-to-azure#replicated-machines'>visit here</a>."
		}, {
			"id": "problem_source_machine_name",
			"order": 4,
			"controlType": "textbox",
			"displayLabel": "What is the name of the VM that you are trying to protect?",
			"useAsAdditionalDetails": false,
			"required": false
		}, {
			"id": "learn_more_text_2",
			"order": 5,
			"controlType": "infoblock",
			"content": "<b>Review steps listed below, provide the STATUS and check the links below to find resolutions to common issues:</b>"
		}, {
      "id": "Replication not progressing issues",
      "order": 6,
      "controlType": "dropdown",
      "displayLabel": "I am trying to Enable Replication for my VM(s), but",
      "watermarkText": "Choose the problem that you are facing",
      "dropdownOptions": [{
        "value": "Replication is stuck at 0%",
        "text": "Replication is stuck at 0%"
          }, {
          "value": "Replication is stuck at >0%",
          "text": "Replication is stuck at >0%"
          }, {
          "value": "VM is protected,but Replication health is critical",
          "text": "VM is protected, but Replication health is critical"
          }, {
          "value": "Application Consistent Snapshot is missing/not latest",
          "text": "Application Consistent Snapshot is missing/not latest"
          }, {
          "value": "My issue is not listed here",
          "text": "My issue is not listed here"
          }
      ],
      "required": true
      },  {
  				"id": "learn_more_text_5",
  				"order": 7,
  				"controlType": "infoblock",
  				"content": "Replication not progressing? try these <a href='https://docs.microsoft.com/azure/site-recovery/site-recovery-vmware-to-azure-protection-troubleshoot'> troubleshooting</a> steps."
      },  {
      			"id": "learn_more_text_5",
      			"order": 11,
      			"controlType": "infoblock",
      			"content": "Missing/No-latest Application Consistent Snapshot? try these <a href='https://aka.ms/tshootv2anoappconsistentsnapshot'> troubleshooting</a> steps."
      }, {
      "id": "problem_details",
      "order": 8,
      "controlType": "multilinetextbox",
      "displayLabel": "Please provide additional details:",
      "watermarkText": "Paste error message(s), error code(s) and describe the scenario(s) that are failing.",
      "required": true,
      "useAsAdditionalDetails": false
    }
    ]}
