<properties
	pageTitle="NFS 3.0 issues with Azure Blob storage scoping questions"
	description="NFS 3.0 issues with Azure Blob storage scoping questions"
	authors="annayak"
    ms.author="annayak"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32739611,32739612"
	productPesIds="16459"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	articleId="42b389c1-1224-4646-a84f-4687eb6bf600"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>
# NFS 3.0 issues with Azure Blob storage
---
{
   "subscriptionRequired":true,
   "resourceRequired":true,
   "title":"NFSv3 for blob scoping question",
   "fileAttachmentHint":"",
   "formElements":[
      {
         "id":"problem_type",
         "order":1,
         "controlType":"dropdown",
         "displayLabel":"How would you want us to help you?",
         "watermarkText":"Choose a problem area",
         "dropdownOptions":[
            {
               "value":"Issue",
               "text":"Troubleshoot an NFSv3 for Blob Storage issue"
            },
            {
               "value":"dont_know_answer",
               "text":"Need advisory guidance on NFSv3 for Blob Storage"
            }
         ],
         "required":true
      },
      {
         "id":"problem_start_time",
         "visibility":"problem_type == Issue",
         "order":5,
         "controlType":"datetimepicker",
         "displayLabel":"Local start time of the most recent occurrence",
         "required":true
      },
      {
         "id":"blob_container",
         "order":10,
         "visibility":"problem_type == Issue",
         "controlType":"dropdown",
         "displayLabel":"Blob Container",
         "watermarkText":"Choose an option",
         "dynamicDropdownOptions":{
            "uri":"/subscriptions/{subscriptionid}/resourceGroups/{resourcegroup}/providers/Microsoft.Storage/storageAccounts/{resourcename}/blobServices/default/containers?api-version=2018-07-01",
            "jTokenPath":"value",
            "textProperty":"id",
            "valueProperty":"id",
            "textPropertyRegex":"[^/]+$",
            "defaultDropdownOptions":{
               "value":"dont_know_answer",
               "text":"None of the above"
            }
         },
         "DropdownOptions":[
            {
               "value":"NoBlobContainer",
               "text":"Not specific to a blob container"
            }
         ],
         "required":true
      },
      {
         "id":"issue_nature",
         "order":15,
         "visibility":"problem_type == Issue",
         "controlType":"dropdown",
         "displayLabel":"What error did you get?",
         "watermarkText":"Choose the error that you got",
         "dropdownOptions":[
            {
               "value":"Issue_AccessDenied",
               "text":"Access Denied"
            },
            {
               "value":"Issue_NoSuchFileOrDirectory",
               "text":"No such file or directory"
            },
            {
               "value":"Issue_ConnectionTimedOut",
               "text":"Connection timed out"
            },
            {
               "value":"Issue_MountPointDoesntExist",
               "text":"mount point does not exist"
            },
            {
               "value":"Issue_NoSuchFileOrDirectory",
               "text":"mount: bad option"
            },
            {
               "value":"Issue_NoSuchFileOrDirectory",
               "text":"mount.nfs: Remote I/O error"
            },
            {
               "value":"Issue_NoSuchFileOrDirectory",
               "text":"mount.nfs: an incorrect mount option was specified"
            },
            {
               "value":"Issue_NoSuchFileOrDirectory",
               "text":"mount.nfs: Connection timed out"
            },
            {
               "value":"Issue_NoSuchFileOrDirectory",
               "text":"mount.nfs: Stale file handle"
            },
            {
               "value":"Issue_NoSuchFileOrDirectory",
               "text":"not able to list a recently added file"
            },
            {
               "value":"Issue_NoSuchFileOrDirectory",
               "text":"requested NFS version or transport protocol is not supported"
            },
            {
               "value":"dont_know_answer",
               "text":"Got some other error"
            }
         ],
         "required":true
      },
      {
         "id":"Linux_distro",
         "order":20,
         "visibility":"problem_type == Issue",
         "controlType":"dropdown",
         "displayLabel":"Linux distro being used",
         "watermarkText":"Select the Linux distro being used",
         "dropdownOptions":[
            {
               "value":"Linux_Ubuntu",
               "text":"Ubuntu Server"
            },
            {
               "value":"Linux_RHEL",
               "text":"Red Hat Enterprise Linux"
            },
            {
               "value":"Linux_SUSE",
               "text":"SUSE Enterprise Linux"
            },
            {
               "value":"Linux_CentOS",
               "text":"CentOS-based Linux"
            },
            {
               "value":"Linux_Debian ",
               "text":"Debian"
            },
            {
               "value":"Linux_Oracle",
               "text":"Oracle Linux"
            },
            {
               "value":"dont_know_answer",
               "text":"Other distro"
            }
         ],
         "required":true
      },
      {
         "id":"Distro_Version",
         "order":25,
         "visibility":"problem_type == Issue",
         "controlType":"textbox",
         "displayLabel":"Linux Distro Version",
         "watermarkText":"To find distro version - cat /etc/os-release",
         "textPropertyRegex":"^\\d+(\\.\\d+)*$",
         "required":false
      },
      {
         "id":"NFS_Error",
         "order":30,
         "visibility":"problem_type == Issue",
         "controlType":"dropdown",
         "displayLabel":"NFSv3 Returned Error Code",
         "watermarkText":"Select the error code received",
         "dropdownOptions":[
            {
               "value":"NFS3ERR_PERM",
               "text":"NFS3ERR_PERM"
            },
            {
               "value":"NFS3ERR_NOENT ",
               "text":"NFS3ERR_NOENT "
            },
            {
               "value":"NFS3ERR_IO",
               "text":"NFS3ERR_IO"
            },
            {
               "value":"NFS3ERR_NXIO",
               "text":"NFS3ERR_NXIO"
            },
            {
               "value":"NFS3ERR_ACCES",
               "text":"NFS3ERR_ACCES"
            },
            {
               "value":"NFS3ERR_EXIST",
               "text":"NFS3ERR_EXIST"
            },
            {
               "value":"NFS3ERR_XDEV",
               "text":"NFS3ERR_XDEV"
            },
            {
               "value":"NFS3ERR_NODEV",
               "text":"NFS3ERR_NODEV"
            },
            {
               "value":"NFS3ERR_NOTDIR",
               "text":"NFS3ERR_NOTDIR"
            },
            {
               "value":"NFS3ERR_ISDIR",
               "text":"NFS3ERR_ISDIR"
            },
            {
               "value":"NFS3ERR_INVAL",
               "text":"NFS3ERR_INVAL"
            },
            {
               "value":"NFS3ERR_FBIG",
               "text":"NFS3ERR_FBIG"
            },
            {
               "value":"NFS3ERR_NOSPC",
               "text":"NFS3ERR_NOSPC"
            },
            {
               "value":"NFS3ERR_ROFS",
               "text":"NFS3ERR_ROFS"
            },
            {
               "value":"NFS3ERR_NODEV",
               "text":"NFS3ERR_NODEV"
            },
            {
               "value":"NFS3ERR_MLINK",
               "text":"NFS3ERR_MLINK"
            },
            {
               "value":"NFS3ERR_NAMETOOLONG",
               "text":"NFS3ERR_NAMETOOLONG"
            },
            {
               "value":"NFS3ERR_NOTEMPTY",
               "text":"NFS3ERR_NOTEMPTY"
            },
            {
               "value":"NFS3ERR_DQUOT",
               "text":"NFS3ERR_DQUOT"
            },
            {
               "value":"NFS3ERR_STALE",
               "text":"NFS3ERR_STALE"
            },
            {
               "value":"NFS3ERR_REMOTE",
               "text":"NFS3ERR_REMOTE"
            },
            {
               "value":"NFS3ERR_BADHANDLE",
               "text":"NFS3ERR_BADHANDLE"
            },
            {
               "value":"dont_know_answer",
               "text":"dont know error"
            }
         ],
         "required":false
      },
      {
         "id":"xid",
         "order":35,
         "visibility":"problem_type == Issue",
         "controlType":"textbox",
         "displayLabel":"Error XID - Can be found in network trace",
         "watermarkText":"Error XID - Can be found in network trace",
         "textPropertyRegex":"[0-9]$",
         "required":false
      },
      {
         "id":"problem_description",
         "order":40,
         "controlType":"multilinetextbox",
         "displayLabel":"Provide details of your advisory ask. For troubleshooting issues provide additional details like error message or exception stack",
         "required":true,
         "useAsAdditionalDetails":true
      }
   ],
   "$schema":"SelfHelpContent"
}
---