<properties
	  pageTitle="Connection Debug Troubleshooting"
	  description="Connection Debug Troubleshooting"
      service="Microsoft.DocumentDB"
      resource="databaseAccounts"
	  authors="anferrei"
	  ms.author="anferrei"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="a9f7b533-6634-4392-9a31-8e05b694ad21"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Connection Debug Troubleshooting

<!--issueDescription-->

Dear customer, 

We have reviewed your case and we need additional information to help aid you with a fast investigation, please provide us with the following:

1. Repro script that you are using to reliably reproduce the issue
2. Actual client logs for failed operation
3. Timestamp or time range when the failure happened
4. If you are unable to issue requests to the account please run the below commands based on your environment and provide the results (for both port 10250 and 10255):  
??a. On Windows 8/Win 2012 and later (only if the you don't want to install)
b. Powershell Test-NetConnection -ComputerName <accountName>.documents.azure.com -Port 10250 -InformationLevel Detailed

###On Unix systems
nc -v <accountName>.documents.azure.com 10250

###On Azure Web apps/Windows platforms (recommended tool)
Use psping utility:
https://technet.microsoft.com/en-us/sysinternals/psping.aspx

Usage example:
C:\tools\pstools>psping 40.118.245.44:10250

If the above commands indicate that the TCP connect to port 10250/10255 fails, then there is a firewall in your environment which is blocking the connection to Azure Cosmos DB and need to be worked out with your IT team.  

**Note:*** If the you are successfully able to ping using the above tools, check for SSL version used as below

##SSL Handshake failure:
If the commands in the initial steps above are successful, it could still be a problem with SSL negotiation.  Cosmos DB only supports TLSv1.2, which is available on OpenSSL1.0+ .  Please do the below checks and capture output of each to share with the Product team

###Checking OpenSSL version
Run the "openssl version" command to check what is the version.  His version should be higher than 1.0.2

###Check the SSL negotiated via the browser
Open a browser and go to https://www.howsmyssl.com/.  It will display the entire SSL handshake payload done by the client.  Check if says that TLS v1.2 was used (below output).  If not, upgrade openssl library version.

###For OSX/Mac clients 
OSX ships with an older version of openssl which does not support TLSv1.2.  You needs to update the OpenSSL package shipped with the operating system
- More details at
https://apple.stackexchange.com/questions/126830/how-to-upgrade-openssl-in-os-x 
http://techiezone.rottigni.net/2016/03/python-2-7-11-on-el-capitan-with-tls-1-2-support

###For Java applications (Azure WebApp and others) 
Even if the OpenSSL version is correct, Java 7 runtime does not enable TLSv1.2 by default.  The WebApp (Tomcat or others) need to be setup to use TLS v1.2 instead of SSL 3 using the below references.  Another option is to upgrade the web app to use Java 8 which does not have the same problem and uses TLSv1.2 by default.

###For references and command line information for Java 7, please use
- https://social.msdn.microsoft.com/Forums/silverlight/en-US/ea9c7245-6f78-42e6-a772-f1fe83107d32/sslhandshakeexception-from-azure-web-app-spring-rest-to-mongodb?forum=AzureDocumentDB
- https://superuser.com/questions/747377/enable-tls-1-1-and-1-2-for-clients-on-java-7   
- https://stackoverflow.com/questions/9749339/does-tomcat-support-tls-v1-2   
- http://fsanglier.blogspot.com/2015/04/java-7-and-tlsv12-supported-but-not-enabled.html   

###For nodejs and its derivatives (like mongoose)
Run the below script and check if the output contains "Your client is using TLS1.2" (or share the output)

```
import ssl, urllib2

ctx = ssl.SSLContext(ssl.PROTOCOL_TLSv1_2)

url = "https://www.howsmyssl.com/"

response = urllib2.urlopen(url, context=ctx).read()
```

###For python
Run the below script and check if the output contains " u'tls_version': u'TLS 1.2".  Please capture and save the entire output

```
>>> import requests

>>> r = requests.get('https://www.howsmyssl.com/a/check')

>>> r.json()
```

<br>
 

###For php

Run the below command to check the openssl version which which the current php subsystem was compiled with

```
<?php
echo "openssl version text: " . OPENSSL_VERSION_TEXT . "\n";
echo "openssl version number:  " . OPENSSL_VERSION_NUMBER . "\n";
?>
```
 
Make a curl request to www.howsmyssl.com (follow https://stackoverflow.com/questions/27904854/verify-if-curl-is-using-tls)

```
<?php

$ch = curl_init('https://www.howsmyssl.com/a/check');

curl_setopt($ch, CURLOPT_RETURNTRANSFER, true);

$data = curl_exec($ch);

curl_close($ch);

$json = json_decode($data);

echo $json->tls_version;
```

Thank you.

<!--/issueDescription-->

