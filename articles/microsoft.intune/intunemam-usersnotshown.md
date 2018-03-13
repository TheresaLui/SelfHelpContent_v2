<properties 
    pageTitle="App reporting by user does not show new targeted users for the app protection policy"
    description="App reporting by user does not show new targeted users for the app protection policy"
    service="microsoft.intune"
    resource="intune"
    authors="JordanWallach"
    displayOrder="4"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="mam, mampolicy"
    productPesIds=""
    cloudEnvironments="public"
 />

# App reporting by user does not show new targeted users for the app protection policy

## **Recommended steps**
It can take up to 24 hours for a new targeted user to show up in reports. Policy changes/updates can take up to 8 hours to apply.<br>

You can force an app to sync with the service, which will shorten the time to apply the policy and show the user in reports. For some apps, logging out and logging back in will force a sync. Other apps, such as Outlook, require you to delete the user account and then recreate the account to force the sync.