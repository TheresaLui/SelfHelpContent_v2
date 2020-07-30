<properties pageTitle="Unable to connect to the mounted Azure Files Drive"
            description="Unable to connect to the mounted Azure Files Drive"
            service="Microsoft.Storage"
            resource="Microsoft.Storage/storageAccounts"
            authors="akshaymatmicrosoft"
            ms.author="akshaym"
            displayOrder=""
            selfHelpType="TSG_Content"
            supportTopicIds=""
            resourceTags=""
            productPesIds=""
            cloudEnvironments="public, fairfax, usnat, ussec"
            articleId="d46d5e19-2d00-4686-9d8e-3f58a5279269"
            ownershipId="Centennial_CloudNet_LoadBalancer" />


# Unable to connect to the mounted Azure Files Drive

**Symptom**

Customer complaints that his application or service is unable to connect to the mounted Azure Files Drive.

**Cause**

Drives are mounted per user, if the application/service is running under different user context, it won't see the Azure Files mounted drive.

**Resolution**

To resolve the issue, follow the instructions:

1. Mount drive from the same user context that the application is running. You can use tools such as '```psexec```' to do this.
2. Run the '```net use```' command after you run the command '```psexec -i -s cmd.exe```' in elevated mode to mount the drive under **system** context (as described in step 3)
3. Run the '```net use```' command after you run the command '```psexec -i -u UserName cmd.exe```' in elevated mode to mount the drive under a specific **user** context

**Note**: If you are uncertain whether you are running the application in the context of the user who mapped the drive, please try running '```net use```' with '```psexec```' as described in the previous steps, Or:

    1. You can create a new user with the same permission as the network service or system account, and run '```cmd```' and '```net use```' under that user. The username should be the storage account name, and password should be the storage account key.
    2. Another option for '```net use```' is to pass in the storage account name and key in the username and password parameters of the '```net use```' command

**More information**

After following the above instructions, if you receive error "**System error 1312 has occurred. A specified logon session does not exist. It may already have been terminated.**" with '```net use```' for the system/network service account, ensure that the username passed to '```net use```' includes domain information e.g. "[storage account name].file.core.windows.net".

<!---

---
**This is the end of the work flow. Did this TSG resolve your issue?**

1. Yes
2. No

-->
