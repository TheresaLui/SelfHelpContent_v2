<properties
	pageTitle="AD DS authentication over SMB"
	description="AD DS authentication over SMB"
	ms.author="kashah"
	displayOrder=""
	selfHelpType="Apollo"
	supportTopicIds="7261aa6c-f772-babc-331c-9f0ff6f82e7f"
	resourceTags=""
	productPesIds="16460"
	cloudEnvironments="public"
	articleId="bf736888-9e26-4600-995e-7a2362eea07b"
	ownershipId="StorageMediaEdge_StorageFiles"
/>
# Enabling AD DS Authentication for Azure Files
## Enable AD DS authentication for Azure Files
:::Section Recommended Solution:::

Azure Files supports identity-based authentication over Server Message Block (SMB) through two types of Domain Services: on-premises Active Directory Domain Services (AD DS) and Azure Active Directory Domain Services (Azure AD DS). This series of articles and videos focus on enabling and configuring on-premises AD DS for authentication with Azure File Shares:

1. Before you enable AD DS authentication for Azure Files, review the [prerequisites](https://docs.microsoft.com/azure/storage/files/storage-files-identity-auth-active-directory-enable#prerequisites/)
2. Configure your [networking end points](https://docs.microsoft.com/azure/storage/files/storage-files-networking-endpoints?tabs=azure-portal) and [DNS forwarding](https://docs.microsoft.com/azure/storage/files/storage-files-networking-dns)
3. Set up the [AD DS authentication for Azure Files](https://docs.microsoft.com/azure/storage/files/storage-files-identity-ad-ds-enable/)
4. Watch this video on enabling AD DS authentication for Azure Files with private endpoints and DNS forwarding:
	<videoGroup>
	<video>
	<src>https://sec.ch9.ms/ch9/3358/0addac01-3606-4e30-ad7b-f195f3ab3358/ITOpsTalkAzureFiles_high.mp4</src>
	<title>Step by Step guidance for enabling Files AD DS Authentication with private endpoints</title>
	</video>
	</videoGroup>

5. Enable AD DS authentication for Azure files with [Windows Virtual Desktop](https://docs.microsoft.com/azure/virtual-desktop/create-file-share/):
	<videoGroup>
	<video>
	<src>https://www.youtube.com/watch?v=9S5A1IJqfOQ</src>
	<title>Step by Step guidance for enabling Files AD DS Authentication with Windows Virtual Desktop</title>
	</video>
	</videoGroup>

