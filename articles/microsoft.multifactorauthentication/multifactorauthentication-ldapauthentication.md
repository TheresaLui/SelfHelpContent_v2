<properties  
    pageTitle="MFA Server (On-Premises)/LDAP authentication" 
    description=" LDAP authentication" 
    service="microsoft.multifactorauthentication" 
    resource="" 
    authors="kgremban" 
    selfHelpType="generic" 
    supportTopicIds="32336320" 
    productPesIds="14947" 
    cloudEnvironments="public" 
    	articleId="d0645755-ffa3-460e-b5af-8570062721d1"
/> 
# LDAP authentication 

## **Recommended steps** 

Ensure that the IP Address you entered in the MFA server when you added the LDAP client is the IP that requests are coming from, especially if there are multiple NICs/addresses on the device being secured.  A packet capture should allow you to see this information. The capture should also allow you to confirm that communication is occurring through the firewall. 

In the Directory Integration section, ensure you have the target LDAP server configured properly:
   
- The server can be hostname or IP. If you want to specify multiple servers, then a back-up may be specified separated by a semicolon. 
- The base DN should be where you want to query in the directory. For example, dc=domain,dc=com. 
- If using SSL, test with simple or windows first to make sure communication is working.  If it works, then there may be an issue with the certificate you are using. Ensure it’s installed locally and trusted by your LDAP directory. 
- The bind username and password is set per machine, as it’s stored in the local windows store.  If you have multiple MFA servers you need to enter this in each server that you wish to process LDAP auth. 
- Use the test button to ensure communication.  This ensures you can bind.  You can also go to the users section and select a user to test against LDAP auth to test an auth for a specific user as well. 

## **Recommended documents** 

- [LDAP Authentication and Azure Multi-Factor Authentication](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started-server-ldap) 
- [Directory Integration between Azure MFA Server and AD/LDAP](https://docs.microsoft.com/azure/multi-factor-authentication/multi-factor-authentication-get-started-server-dirint) 
- [Azure MFA Server Video Overview](https://azure.microsoft.com/resources/videos/multi-factor-authentication-server) 
