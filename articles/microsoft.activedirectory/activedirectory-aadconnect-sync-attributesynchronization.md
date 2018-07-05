<properties
	pageTitle="Synchronizing AD to Azure AD/Synchronization problem for a specific attribute"
	description="Synchronizing AD to Azure AD/Synchronization problem for a specific attribute"
	service="microsoft.activedirectory"
	resource="activedirectory"
	authors="cychua"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32565590"
	resourceTags=""
	productPesIds="14785"
	cloudEnvironments="public"
/>

# Synchronizing AD to Azure AD/Synchronization problem for a specific attribute

## Recommended steps

**How to select specific attributes to synchronize to Azure AD**

  * For information about the list of attributes synchronized by Azure AD Connect, refer to article [Azure AD Connect sync: Attributes synchronized to Azure Active Directory](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-attributes-synchronized).

  * If you would like to limit the list of attributes synchronized to Azure AD, refer to article section [Custom installation of Azure AD Connect - Azure AD app and attribute filtering](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-get-started-custom#azure-ad-app-and-attribute-filtering).

**Issue with certain attributes not synchronized to Azure AD**

Important points to consider:

  * If you recently updated the list of attributes to be synchronized to Azure AD, you must remember to do a Full import, followed by Delta synchronization.
  
  * If you recently updated your on-premises AD schema with new AD attributes and you want those attributes to synchronize to Azure AD, you must first refresh the schema in Azure AD Connect before those attributes can be included for Directory Synchronization.
  
  * If you have issues with synchronizing on-premises Exchange AD attributes (msExch-) to Azure AD for some User objects, be sure to check if mailNickname attribute on the User object is populated. By default, Exchange AD attributes are not flown unless the mailNickname attribute on the User object is assigned a value.

**Issue with LargeObject errors**

  * When an attribute exceeds the allowed size limit, length limit or count limit set by Azure Active Directory schema, the synchronization operation results in the LargeObject or ExceededAllowedLength sync error. Typically this error occurs for the following attributes:
    * userCertificate
    * userSMIMECertificate
    * thumbnailPhoto
    * proxyAddresses

  * For userCertificate and userSMIMECertificate attributes, Azure AD enforces a maximum limit of 15 values on each attribute. For details on how to troubleshoot LargeObject errors related to userCertificate, refer to article [Handling LargeObject errors caused by userCertificate attribute](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-largeobjecterror-usercertificate).

  * For thumbnailPhoto attribute, Azure AD enforces a maximum size limit of 100KB.

  * For proxyAddresses, Azure AD does not currently enforce a hard limit on the attribute itself. However, Azure AD only permits up to 1000 attribute values on a given User object. This includes all attributes including system attributes which are not always visible to customers.
  
