<properties
    pageTitle="Administrator-initiated password reset"
    description="Password Management/Administrator-initiated password reset"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="zhchia, gahug"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32045781"
    resourceTags=""
    productPesIds="14785"
    cloudEnvironments="public"
    />

# I'm having problems resetting a user's password

## **Recommended steps**

**I'm having a problem resetting a user's password**

*  Make sure you are authorized to reset passwords. *Only global, password, and user administrators can reset user passwords.* Global administrators can also reset other privileged administrator's passwords.

* Make sure you that you understand the licensing requirements:
  * You must have at least one license assigned in your organization
    * **Cloud only users** - Any Office 365 (O365) paid SKU, or Azure AD Basic
    * **Cloud and/or on-premises users** - Azure AD Premium P1 or P2, Enterprise Mobility + Security (EMS), or Secure Productive Enterprise (SPE)
    * Click [here](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-licensing) to read more about licensing requirements.


* To reset a user's password, find the user in Azure AD. Then, on the overview blade for that user, click the "reset password" button


**The password reset button is greyed-out**

* You are not authorized to reset **this** user's passwords. *Only global, password, and user administrators can reset user passwords.* Global administrators can also reset other privileged administrator's passwords.


**I don't see the password reset blade**

* You are not authorized to reset passwords. *Only global, password, and user administrators can reset user passwords.* Global administrators can also reset other privileged administrator's passwords.


**I don't see the on-premises integration blade in password reset**

* The on-premises integration blade only appears in hybrid environments - meaning you are using password writeback to manipulate on-premises user's passwords.

* You will not see this blade if:
  * You are not using password writeback
  * There is a problem with your installation/connectivity of password writeback
  * There is a problem with your installation/connectivity of Azure AD Connect
  * Click [here](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#troubleshoot-password-writeback) to troubleshoot issues with password writeback


**I don't know how to reset a user's password**

1. Sign in to the Azure portal as an appropriate admin.
2. Go to the **Users and groups** blade, select **All Users**
3. Select a user from the list.
4. For the selected user, select **Overview**, and then in the command bar, select **Reset password**.
5. Select the **Reset password** button and follow the instructions on the screen.
  * Only resets performed through the **Azure portal** support password writeback.


**I reset an on-premises user's password from the Office 365 Admin portal or Office 365 mobile application but the user is still not able to sign-in**

* Password Writeback is not supported in this portal. Please reset the user's password again in the new Azure portal - [portal.azure.com](https://portal.azure.com/)


<!-- **I reset an on-premises user's password from the Azure Classic portal but the user is still not able to sign-in**

* Password Writeback is not supported in this portal. Please reset the user's password again in the new Azure portal - [portal.azure.com](https://portal.azure.com/) -->


## **Recommended documents**
<!--
 John Flores is working on a new version of this doc. Once that is live will reactivate/update link

 * [Top Tips from our customers](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#top-tips-from-our-customers-to-read-before-you-begin) -->
* [Getting Started with Password Reset](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#enable-users-to-reset-their-azure-ad-passwords)
* [Troubleshoot Administrator-initiated Password Reset](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#troubleshoot-the-password-reset-portal)
* [FAQ - Password Reset](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-faq)
* [Information to include when you need help](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#contact-microsoft-support)
