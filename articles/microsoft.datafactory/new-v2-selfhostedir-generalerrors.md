<properties
	pageTitle="Self-hosted IR general failure or errors"
	description="Integration Runtime fails to copy data to/from an on-premises data store"
	infoBubbleText=""
	authors="hecepeda"
	ms.author="hecepeda"
	articleId="new-v2-selfhostedir-generalerrors.md"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32637155"
	resourceTags=""
	productPesIds="15613"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_DataFactory"
/>

# Self-hosted IR general failure or error

**Note:** Please follow the steps on the [troubleshooting guide](https://docs.microsoft.com/azure/data-factory/self-hosted-integration-runtime-troubleshoot-guide#gather-self-hosted-integration-runtime-logs-from-azure-data-factory), and take note of the **Report ID** to provide it with the support request.

### __TLS/SSL certificate issue__

__Symptoms__

When trying to enable TLS/SSL certificate (advanced) from *Self-hosted IR Configuration Manager* -> *Remote access from intranet*, after selecting TLS/SSL certificate, below error shows up:

```
Remote access settings are invalid. Identity check failed for outgoing message. The expected DNS identity of the remote endpoint was ‘abc.microsoft.com’ but the remote endpoint provided DNS claim ‘microsoft.com’. If this is a legitimate remote endpoint, you can fix the problem by explicitly specifying DNS identity ‘microsoft.com’ as the Identity property of EndpointAddress when creating channel proxy.
```

In above case, the user is using certificate with "microsoft.com" as last item.

__Cause__

This is a known issue in WCF: WCF TLS/SSL validation only checks last DNSName in SAN.

__Resolution__

Wildcard certificate is supported in Azure Data Factory v2 Self-hosted IR. This issue normally happens because the SSL certificate is not correct. The last DNSName in SAN should be valid. Follow steps below to verify it.

1. Open Management Console, double check both Subject and Subject Alternative Name from the Certificate Details. In above case, for example, the last item in Subject Alternative Name, which is "DNS Name= microsoft.com.com", is not legitimate.
1. Contact the certificate issue company to remove the wrong DNS Name

### __Concurrent jobs limit issue__

__Symptoms__

When trying to increase the limit concurrent jobs from the Azure Data Factory UI, it hangs as _updating_ forever. The max value of concurrent jobs was set to 24 and you want to increase the count so that jobs can run faster. The minimum value that you can enter is 3 and the maximum value that you can enter is 32. You increased the value from 24 to 32 and hit on update button, in the UI it got stuck on updating. After refreshing, the customer still saw the value as 24 and it never got updated to 32.

__Cause__

There is a limitation for the setting as the value depends on the computer logicCore and Memory, you can just adjust it to a smaller value such as 24 and see the result.

### __Self-hosted IR HA SSL Certificate issue__

__Symptoms__

Self-hosted IR work node has reported the error below:

```
Failed to pull shared states from primary node net.tcp://abc.cloud.corp.Microsoft.com:8060/ExternalService.svc/. Activity ID: XXXXX The X.509 certificate CN=abc.cloud.corp.Microsoft.com, OU=test, O=Microsoft chain building failed. The certificate that was used has a trust chain that cannot be verified. Replace the certificate or change the certificateValidationMode. The revocation function was unable to check revocation because the revocation server was offline.
```

__Cause__

When we handle cases related to SSL/TLS handshake, we might encounter some issues related to certificate chain verification.

__Resolution__

* Here is a quick and intuitive way to troubleshoot X.509 certificate chain build failure:

  1. Export the certificate, which needs to be verified. Go to manage computer certificate and find the certificate that you want to check and right-click **All tasks** -> **Export**.
  1. Copy the exported certificate to the client machine
  1. On the client side, run below command in CMD. Make sure that you have replaced below _<certificate path>_ and _<output txt file path>_ placeholders with related paths:

    ```
    Certutil -verify -urlfetch <certificate path> > <output txt file path>
    ``` 

    For example:

    ```
    Certutil -verify -urlfetch c:\users\test\desktop\servercert02.cer > c:\users\test\desktop\Certinfo.txt
    ```

  4. Check if there is any error in the output txt file. You can find the error summary at the end of the txt file.

    For example:

    ```
    ERROR: Verifying leaf certificate revocation status returned The revocation function was unable to check revocation because the revocation server was offline. 0c80092013 (-2146885613 CRYPT_E_REVOCATION_OFFLINE)
    CertUtil: The revocation function was unable to check revocation because the revocation server was offline.
    ```

    If you do not see any error at the end of the log file, you can consider the certificate chain built up successfully in the client machine.

* If there is AIA, CDP and OCSP configured in the certificate file, we can check it in a more intuitive way:

  1. You can get this info by checking the details of a certificate
  1. Run below command. Make sure that you have replaced `<certificate path>` placeholder with related path of the certificate:

    ```
    Certutil -URL <certificate path> 
    ```

  3. Then the *URL Retrieval tool* will be opened. You can verify certificates from AIA, CDP, and OCSP by clicking the *Retrieve* button.

  The certificate chain can be built up successfully if the certificate from AIA is "Verified", and the certificate from CDP or OCSP is "Verified".

  If you see failure when retrieving AIA, CDP, work with network team to get the client machine ready to connect to target URL. It will be enough if either the http path or the ldap path is able to be verified.

### __Self-hosted IR could not load file or assembly__

__Symptoms__

```
Could not load file or assembly 'XXXXXXXXXXXXXXXX, Version=4.0.2.0, Culture=neutral, PublicKeyToken=XXXXXXXXX' or one of its dependencies. The system cannot find the file specified. Activity ID: 92693b45-b4bf-4fc8-89da-2d3dc56f27c3
```

For example:

```
Could not load file or assembly 'System.ValueTuple, Version=4.0.2.0, Culture=neutral, PublicKeyToken=XXXXXXXXX' or one of its dependencies. The system cannot find the file specified. Activity ID: 92693b45-b4bf-4fc8-89da-2d3dc56f27c3
```

__Cause__

If you take process monitor, you can see PATH NOT FOUND errors on files accessed from the GAC or Integration Runtime installation path (ie. *System.ValueTuple.dll*)

 > **Tip**<br>
 >You can set a filter on the Path column using the file name like *System.ValueTuple*, you will see the file is not located in GAC related folder, or in `C:\Program Files\Microsoft Integration Runtime\4.0\Gateway`, or in `C:\Program Files\Microsoft Integration Runtime\4.0\Shared` folder. Basically, it will load the dll from _GAC_ folder first, and then from _Shared_ and finally from _Gateway_ folder. Therefore, you can put the dll to any path which can be helpful.


__Resolution__

You can find that the *System.ValueTuple.dll* is located at `C:\Program Files\Microsoft Integration Runtime\4.0\Gateway\DataScan` folder. Copy the *System.ValueTuple.dll* to `C:\Program Files\Microsoft Integration Runtime\4.0\Gateway` folder to resolve the issue.

You can use the same method to solve other file or assembly missing issues.

### __How to audit Self-hosted IR key missing__

__Symptoms__

The self-hosted integration runtime suddenly goes to offline without key, below error message shows in the Event Log: `Authentication Key is not assigned yet`

__Cause__

* The Self-hosted IR node or logical Self-hosted IR in portal is deleted.
* A clean uninstall is done.<br>

__Resolution__

If neither of the above causes applies, you can go to the folder: `%programdata%\Microsoft\Data Transfer\DataManagementGateway`, and check whether the file named *Configurations* is deleted. If it's deleted, follow the instructions [here](https://www.netwrix.com/how_to_detect_who_deleted_file.html) to audit who deletes the file.

### __Cannot use Self-hosted IR to bridge two on-premises data stores__

__Symptoms__

After creating Self-hosted IRs for both source and destination data stores, you want to connect the two IRs together to finish a copy. If the data stores are configured in different VNETs, or they cannot understand the gateway mechanism, you will hit errors like: _the driver of source cannot be found in destination IR; the source cannot be accessed by the destination IR_.

__Cause__

The Self-hosted IR is designed as a central node of a copy activity, not a client agent that needs to be installed for each data store.

In above case, the linked service for each data store should be created with the same IR, and the IR should be able to access both data stores through network. No matter the IR is installed with source data store, destination data store, or on a third machine, if two linked services are created with different IRs, but used in the same copy activity, the destination IR will be used, and the drivers for both data stores need to be installed on the destination IR machine.

__Resolution__

Install drivers for both source and destination on the destination IR, and make sure it can access the source data store.

If the traffic cannot pass through the network between two data stores (for example, they are configured in two VNETs), you may not finish the copy in one activity even with IR installed. In that case, you may create two copy activities with two IRs, each in a VENT: 1 IR to copy from data store 1 to Azure Blob Storage, another to copy from Azure Blob Storage to data store 2. This could simulate the requirement to use the IR to create a bridge that connects two disconnected data stores.

### __Credential sync issue causes credential lost from HA__

__Symptoms__

The data source credential "XXXXXXXXXX" is deleted from current Integration Runtime node with payload "when you delete the link service on Azure portal, or the task has the wrong payload, please create new link service with your credential again".

__Cause__

Your Self-hosted IR is built in HA mode with two nodes, but they are not in credentials sync state, which means the credentials stored in dispatcher node aren't synced to other worker nodes. If any failover happens from dispatcher node to worker node but the credentials only existed in previous dispatcher node, the task will fail when trying to access credentials, and you will hit above error.

__Resolution__

The only way to avoid this issue is to make sure two nodes are in credentials sync state. Otherwise you have to reinput credentials for new dispatcher.

### __Cannot choose the certificate due to private key missing__
__Symptoms__

Import a PFX file to the certificate store.

When selecting the certificate through IR Configuration Manager UI, you hit below error:

```
Failed to change Intranet communication encryption mode: It is likely that certificate '              ' may not have a private key that is capable of key exchange or the process may not have access rights for the private key. Please see inner exception for detail.
```

__Cause__

The user account is in low privilege and cannot access private key.
The certificate was generated as signature but not as key exchange.

__Resolution__

Use a privileged account that can access private key to operate the UI.

Run below command to import the certificate:

```
certutil -importpfx FILENAME.pfx AT_KEYEXCHANGE
```


## **Recommended Documents**

* [Troubleshoot Self-Hosted Integration Runtime](https://docs.microsoft.com/azure/data-factory/self-hosted-integration-runtime-troubleshoot-guide) <br>
* [How to create and configure Self-hosted Integration Runtime](https://docs.microsoft.com/azure/data-factory/create-self-hosted-integration-runtime/), including: <br>
  * [Best Practice](https://docs.microsoft.com/azure/data-factory/create-self-hosted-integration-runtime#installation-best-practices) <br>
  * [Ports and Firewall](https://docs.microsoft.com/azure/data-factory/create-self-hosted-integration-runtime#ports-and-firewall) <br>
  * [Proxy Server](https://docs.microsoft.com/azure/data-factory/create-self-hosted-integration-runtime#proxy-server-considerations) <br>
* [Self-hosted integration runtime](https://docs.microsoft.com/azure/data-factory/concepts-integration-runtime#self-hosted-integration-runtime)<br>
* [Monitor integration runtime](https://docs.microsoft.com/azure/data-factory/monitor-integration-runtime/) <br>
