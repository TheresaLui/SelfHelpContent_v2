<properties
    pageTitle="Customer is facing issues while setting up FSLogix with AD Authentication"
    description="Customer is facing issues while setting up FSLogix with AD Authentication"
    infoBubbleText="Customer is facing issues while setting up FSLogix with AD Authentication"
    service="microsoft.storage"
    resource="storageAccounts"
    authors="yagohel23"
    ms.author="yagohel"
    displayOrder=""
    selfHelpType="Diagnostics"
    supportTopicIds="32689882"
    resourceTags=""
    productPesIds="1003478"
    cloudEnvironments="public,fairfax,blackforest,mooncake,usnat,ussec"
    articleId="df383ba9-5ecc-447e-a3e1-14d887bdf558"
    ownershipID="Centennial_CloudNet_LoadBalancer"
/>

# Customer is facing issues while setting up FSLogix with AD Authentication
<!--issueDescription-->
FSLogix is designed to roam profiles in remote computing environments, such as Windows Virtual Desktop. It stores a complete user profile in a single container.
<!--/issueDescription-->

## **Recommended Steps**

### RBAC Azure permissions

* After you domain-joined the Azure storage account, assign Azure RBAC permissions to Windows Virtual Desktop users
* All users that need to have FSLogix profiles stored on the storage account must be assigned the ***Storage File Data SMB Share Contributor role***
* Users signing in to the Windows Virtual Desktop session hosts need access permissions to access your file share. Granting access to an Azure File share involves configuring permissions both at the share level as well as on the NTFS level, similar to a traditional Windows share.
* The accounts or groups you assign permissions to should have been created in the domain and synchronized with Azure AD. Accounts created in Azure AD won't work.

To assign permissions:

* Open the Azure portal
* Go to the storage account that is domain-joined
* Select Access Control (IAM)
* Select Add a role assignment
* In the Add role assignment tab, select Storage File Data SMB Share Elevated Contributor for the administrator account
* To assign users permissions for their FSLogix profiles, follow these same instructions. However, when you get to step 5, select Storage File Data SMB Share Contributor instead.

### NTFS Windows permissions

Once you've assigned RBAC permissions to your users, next you'll need to configure the NTFS permissions.

- Run the following cmdlet to mount the Azure file share and assign it a drive letter: `net use <desired-drive-letter>: <UNC-pat> <SA-key> /user:Azure\<SA-name>`
- Run the following cmdlets to let your Windows Virtual Desktop users create their own profile containers while blocking access to their profile container from other users:

```
icacls <mounted-drive-letter>: /grant <user-email>:(M)
icacls <mounted-drive-letter>: /grant "Creator Owner":(OI)(CI)(IO)(M)
icacls <mounted-drive-letter>: /remove "Authenticated Users"
icacls <mounted-drive-letter>: /remove "Builtin\Users"
```

For example, `icacls G: /grant john.doe@contoso.com:(M)`.

### Configure FSLogix on client

This section will show you how to configure a VM with FSLogix. You'll need to follow these instructions every time you configure a session host.

There are several options available that ensure the registry keys are set on all session hosts. You can set these options in an image or configure a group policy.
To configure FSLogix on your session host VM:

- RDP to the session host VM of the Windows Virtual Desktop host pool
- Download and install FSLogix [here](https://docs.microsoft.com/fslogix/install-ht)
- Follow the instructions in [Configure profile container registry settings](https://docs.microsoft.com/fslogix/configure-profile-container-tutorial#configure-profile-container-registry-settings):

    * Navigate to Computer > HKEY_LOCAL_MACHINE > SOFTWARE > FSLogix
    * Create a Profiles key
    * Create Enabled, DWORD with a value of 1
    * Create VHDLocations, MULTI_SZ
    * Set the value of VHDLocations to the UNC path you generated in Get the UNC path

* Restart the VM

## Troubleshooting Symptoms

Users profiles are not able to read or write to the storage account as necessary.

### Troubleshooting

At the Azure File Share level, make sure that the WVD Users and WVD Admin have Azure SMB permissions.

### Collaboration

If user needs assistance configuring FSlogix, create a collaboration to FSLogix team: Routing: Windows Servers/Windows Remote Management/FSLogix/Profile

## **Recommended Documents**

* [Create File Share](https://docs.microsoft.com/azure/virtual-desktop/create-file-share)

