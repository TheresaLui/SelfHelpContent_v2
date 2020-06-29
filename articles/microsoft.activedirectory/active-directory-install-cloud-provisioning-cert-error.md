<properties
	pageTitle="Problem installing Cloud Provisioning Agent"
	description="Problem installing Cloud Provisioning agent due to certificate invalidity"
	infoBubbleText="Problem installing Cloud Provisioning agent"
	service="microsoft.aad"
	resource="Microsoft_AAD_IAM"
	ms.author="Dhanyahk"
	displayOrder="2223"
	articleId="943dbd16-aa56-4afa-96d0-77a908d95089"
	diagnosticScenario=""
	selfHelpType="resource"
	supportTopicIds="32689667"
	resourceTags="directory_ad_connect"
	productPesIds="16666"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="AzureIdentity_User"
/>

# Installation issues around Cloud Provisioning due to certificate becoming invalid

You are unable to install the Cloud Provisioning agent (Preview) and getting the error "Time out has expired and the operation has expired".

## **Recommended Steps**

This problem is usually caused by the agent being unable to connect to the Hybrid Identity Service and requires you to configure an HTTP proxy. To resolve this problem, configure an outbound proxy.

1. Sign in to the server with an administrator account
2. Open the agent config file located at <i>C:\Program Files\Microsoft Azure AD Connect Provisioning Agent\AADConnectProvisioningAgent.exe.config</i>
3. Add the following lines into it, toward the end of the file just before the closing `</configuration>` tag. Replace the variables [proxy-server] and [proxy-port] with your proxy server name and port values.

```
<system.net>
        <defaultProxy enabled="true" useDefaultCredentials="true">
            <proxy
                usesystemdefault="true"
                proxyaddress="http://[proxy-server]:[proxy-port]"
                bypassonlocal="true"
            />
        </defaultProxy>
    </system.net>
```

## **Recommended Documents**

* [Troubleshooting additional agent install issues](https://docs.microsoft.com/azure/active-directory/cloud-provisioning/how-to-troubleshoot#agent-problems)
* [Troubleshooting object synchronization issues](https://docs.microsoft.com/azure/active-directory/cloud-provisioning/how-to-troubleshoot#object-synchronization-problems)
* [Troubleshooting sync runs that are in quarantine](https://docs.microsoft.com/azure/active-directory/cloud-provisioning/how-to-troubleshoot#provisioning-quarantined-problems)
