<properties 
    pageTitle="MAM policies are not working for Skype for Business on iOS and Android devices"
    description="MAM policies are not working for Skype for Business on iOS and Android devices"
    service="microsoft.intune"
    resource="intune"
    authors="JordanWallach"
    displayOrder="1"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="mam, mampolicy"
    productPesIds=""
    cloudEnvironments="public"
 />

# MAM policies are not working for Skype for Business on iOS and Android devices

## **Recommended steps**
You have to set up Skype for Business with modern authentication. Follow these steps:

1. Connect to Skype for Business Online using remote PowerShell 
2. Run the following command:<br>
   `Set-CsOAuthConfiguration -ClientAdalAuthOverride Allowed`
3. Verify that the change was successful by running the following:<br>
   `Get-CsOAuthConfiguration` 

## **Recommended documents**

[Skype for Business Online: Enable your tenant for modern authentication](http://social.technet.microsoft.com/wiki/contents/articles/34339.skype-for-business-online-enable-your-tenant-for-modern-authentication.aspx) <br>
[Connecting to Skype for Business Online by using Windows PowerShell](https://aka.ms/SkypePowerShell) <br>
[Get ready to configure mobile app management policies with Microsoft Intune](https://docs.microsoft.com/intune/deploy-use/get-ready-to-configure-mobile-app-management-policies-with-microsoft-intune)
