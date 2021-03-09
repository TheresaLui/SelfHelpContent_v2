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

Azure Files supports identity-based authentication over Server Message Block (SMB) through two types of Domain Services: on-premises Active Directory Domain Services (AD DS) and Azure Active Directory Domain Services (Azure AD DS). The following series of articles and videos focuses on enabling and configuring on-premises AD DS for authentication with Azure File Shares:

1. Before you enable AD DS authentication for Azure Files, review the [prerequisites](https://docs.microsoft.com/azure/storage/files/storage-files-identity-auth-active-directory-enable#prerequisites/)
2. Configure your [networking end points](https://docs.microsoft.com/azure/storage/files/storage-files-networking-endpoints?tabs=azure-portal) and [DNS forwarding](https://docs.microsoft.com/azure/storage/files/storage-files-networking-dns)
3. Set up the [AD DS authentication for Azure Files](https://docs.microsoft.com/azure/storage/files/storage-files-identity-ad-ds-enable/)
4. Watch this video on enabling AD DS authentication for Azure Files with private endpoints and DNS forwarding:
	<video>
	<src>https://www.youtube.com/watch?v=KG0OX0RgytI</src>
	<title>Step-by-step guidance for enabling Files AD DS Authentication with private endpoints</title>
	</video>

5. Enable AD DS authentication for Azure files with [Windows Virtual Desktop](https://docs.microsoft.com/azure/virtual-desktop/create-file-share/):
	<video>
	<src>https://www.youtube.com/watch?v=9S5A1IJqfOQ</src>
	<title>Step-by-step guidance for enabling Files AD DS Authentication with Windows Virtual Desktop</title>
	</video>


### Search your queries related to Azure Files and AD DS Authentication using the below diagnostic

Enabling Azure Files with AD DS Authentication is a multi-step process. Customers need to review detailed documentation for enabling this feature in terms of prerequisites and actual steps.

If you're looking for general guidance on enabling this feature or specific guidance, use the following diagnostic. You can enter your query and the diagnostic will give you an appropriate solution.

Example query: How to enable on-premises AD DS Authentication for Azure Files

<Insight> 
<symptomId>StorageQnaInsight</symptomId> 
<executionText>We are are running a check to determine an accurate response to resolve your issue</executionText> 
<timeoutText>We stopped the check because it was taking too long</timeoutText> 
<noResultText>We are unable to find a response to your query. Rerun the diagnostic and enter a new query</noResultText> 
<additionalInputsReq>true</additionalInputsReq> 
</Insight> 
