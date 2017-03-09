<properties
    pageTitle="Do we have to wrap certs in JSON objects in keyvaults"
    description="Do we have to wrap certs in JSON objects in keyvaults"
    service="scalesets"
    author="negat"
    displayOrder="42"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
    cloudEnvironments="public"
/>

# Do we have to wrap certs in JSON objects in keyvaults?


This is a scale set/VM requirement. We do also support the content type application/x-pkcs12. Instructions found here:
http://www.rahulpnath.com/blog/pfx-certificate-in-azure-key-vault/
 
We currently do not support .cer files, you must export your .cer files into pfx containers.

