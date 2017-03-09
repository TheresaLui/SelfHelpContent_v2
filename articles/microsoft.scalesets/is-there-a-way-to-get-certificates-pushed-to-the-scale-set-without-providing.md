<properties
    pageTitle="Is there a way to get certificates pushed to the scale set without providing the password when the certificate is in SecretStore currently"
    description="Is there a way to get certificates pushed to the scale set without providing the password when the certificate is in SecretStore currently"
    service="scalesets"
    author="negat"
    displayOrder="30"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
    cloudEnvironments="public"
/>

# Is there a way to get certificates pushed to the scale set without providing the password when the certificate is in SecretStore currently?


You do not need to hardcode passwords in scripts; you can dynamically retrieve them with whatever permissions the deployment script you have runs with. If you have a script that is moving a cert from secret store the key vault, the secret store get certificate command also outputs the password of the pfx file.
 