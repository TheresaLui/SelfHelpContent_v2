<properties
    pageTitle="My team works with several certificates that are distributed to us as "
    description="My team works with several certificates that are distributed to us as "
    service="scalesets"
    author="negat"
    displayOrder="39"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
    cloudEnvironments="public"
/>

# My team works with several certificates that are distributed to us as .cer public keys. What is the recommended approach is for deployment of these certs to a scale set?

You can generate a pfx file that only contains .cer files, with X509ContentType = Pfx. For example, load the .cer file as an x509Certificate2 object in C# or PowerShell and calling this method: https://msdn.microsoft.com/library/24ww6yzk(v=vs.110).aspx