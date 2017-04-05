 <properties
	pageTitle="Password Management/Administrator-initiated password reset"
	description="Password Management/Administrator-initiated password reset"
	service="microsoft.activedirectory"
	resource="activedirectory"
	authors="zhchia, gahug"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32045781"
	resourceTags=""
	productPesIds="14785"
	cloudEnvironments="public"
/>

# Password Management/Administrator-initiated password reset
## Pre-Requisites
*  Ensure you are authorized to perform this operation. *Only global, password, and user administrators can reset user passwords.* Global administrators can also reset other privileged administrators passwords. If you are not authorized to perform this task, ask one of the above administrators or use the [self service password reset service](https://passwordreset.microsoftonline.com/)
* Ensure your tenant has a valid license to use Azure AD Self Service Password Reset:
	* Azure AD Premium 1
	* Azure AD Premium 2
	* Enterprise Mobility + Security E3
	* Enterprise Mobility + Security E5
	* Secure Productive Enterprise E3
	* Secure Productive Enterprise E5

## How To
1. Sign in to the Azure portal with an account that is a global admin for the directory the user is in.
2. Select **More Services**, enter **Users and groups** in the text box, and then select **Enter**
3. On the **Users and groups** blade, select **Users**
4. On the **Users and groups - Users** blade, select a user from the list.
5. On the blade for the selected user, select **Overview**, and then in the command bar, select **Reset password**.
6. On the **Reset password** blade, select **Reset password** and follow the instructions on the screen.

*Note: Password Writeback is not supported in the Office Admin portal/O365 admin mobile apps*



## **Recommended documents**
[Top Tips from our customers](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#top-tips-from-our-customers-to-read-before-you-begin) <br>
[Getting Started with Password Management](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started#enable-users-to-reset-their-azure-ad-passwords) <br>
[Troubleshoot Administrator-initiated Password Reset](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#troubleshoot-the-password-reset-portal) <br>
[FAQ - Password Management](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-faq) <br>
[Information to include when you need help](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#information-to-include-when-you-need-help) <br>

<!-- [Azure AD Password Reset for IT Admins](https://docs.microsoft.com/azure/active-directory/active-directory-passwords) <br>
[How Password Reset Works](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-learn-more#how-password-writeback-works) <br>
[How Password Management Works](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-how-it-works) <br>
[Getting Started with Password Management](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-getting-started) <br>
[Troubleshoot Administrator-initiated Password Reset](https://docs.microsoft.com/azure/active-directory/active-directory-passwords-troubleshoot#troubleshoot-the-password-reset-portal) <br> -->
