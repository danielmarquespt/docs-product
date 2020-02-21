---
summary: How to configure OKTA end-user authentication for your applications.
tags: runtime-traditionalweb
---

# Configure OKTA Authentication

OutSystems allows you to use OKTA for authenticating the end-users of your OutSystems applications. This authentication method is configured in a way that is quite similar to the [SAML 2.0](configure-saml.md) one.

 The \[limitations of the current SAML 2.0 implementation\]\(configure-saml.md\#current-limitations\) also apply to the OKTA authentication method. Be sure to check them when using OKTA end-user authentication.

To set up OKTA authentication for end-users do the following:

1. Sign in to the OKTA administration page and make sure that you're using the "Classic UI" view. Select Applications &gt; "Applications" to open the **Applications** screen, and then click **Add Application**.

   ![](../../../../../.gitbook/assets/okta-add-application.jpg)

2. Click **Create New App**.

   ![](../../../../../.gitbook/assets/okta-create-new-app.jpg)

3. Select the platform `Web` and the sign-on method `SAML 2.0`. Click **Create**.

   ![](../../../../../.gitbook/assets/okta-config-1-okta.jpg)

4. Enter a name for your application and \(optionally\) select an app logo. Click **Next**.

   ![](../../../../../.gitbook/assets/okta-config-2-okta.jpg)

5. In the Users application, choose `OKTA` in **Authentication** and fill the **1. Service Provider Connector Settings**.

   We suggest that you use the following values for the fields in the **Attribute Statements \(Claims\)** section:

   Given Name Attribute = `given`  
   Surname Attribute = `surname`  
   Email Attribute = `email`  
   Username Attribute = `username`  
   External Id Attribute = `username`

   ![](../../../../../.gitbook/assets/okta-config-3-users.jpg)

6. Download the keystore certificate by clicking **\(Keystore certificate\)**.  
   This file will be used later when doing the configurations in the OKTA portal \(step 9\).

   ![](../../../../../.gitbook/assets/okta-config-4-users.jpg)

7. In the OKTA portal, configure the fields in General &gt; "SAML Settings" by entering the values for the **Single sign on URL** and **Audience URI \(SP Entity ID\)** fields as displayed or as configured before in the Users application \(step 5\).

   Before continuing, click **Show Advanced Settings** to show some more fields that you will need to configure.

   ![](../../../../../.gitbook/assets/okta-config-5-okta.jpg)

8. Select the **Enable Single Logout** checkbox and fill in the **Single Logout URL** and **SP Issuer** fields with the corresponding values from the Users application.  
   Fill in the **SP Issuer** field with the same value you entered for the **Audience URI \(SP Entity ID\)** field \(step 7\).

   ![](../../../../../.gitbook/assets/okta-config-6-okta.jpg)

9. Upload the certificate file downloaded from the Users application \(step 6\) in the **Signature Certificate** field.

   ![](../../../../../.gitbook/assets/okta-config-7-okta.jpg)

10. In the "Attribute Statements" section, add an attribute for each claim configured in the Users application by clicking **Add Another** until you have a total of four lines of attribute statements.

    Fill in the **Name** and **Value** fields of the four rows according to the following suggested values:

    Name = `given` \(i.e. the value previously entered in Users\) / Value = `user.firstName`  
    Name = `surname` / Value = `user.lastName`  
    Name = `email` / Value = `user.email`  
    Name = `username` / Value = `user.login`

    After creating and filling in the fields, click **Next**.

    ![](../../../../../.gitbook/assets/okta-config-8-okta.jpg)

11. Answer the question **Are you a customer or a partner?** accordingly to your situation and click **Finish**.

    ![](../../../../../.gitbook/assets/okta-config-9-okta.jpg)

12. Right-click the **Identity Provider metadata** link and select **Save Link As** to download the Identity Provider \(IdP\) metadata file.

    ![](../../../../../.gitbook/assets/okta-download-file-okta.jpg)

13. In the Users application, upload the metadata file obtained in the previous step by clicking **Upload from IdP/Federation Metadata XML** and then click **Save**.

    ![](../../../../../.gitbook/assets/okta-upload-file-users.jpg)

14. Test your new authentication settings by logging in the Users application again. Logout of the Users application if you're logged in.
15. The Users application will redirect you to an OKTA login page. Enter your OKTA user credentials.

    If the authentication is successful, you will be redirected to the Users application.

    You may get an "Invalid Permissions" message if the OKTA user is logging in for the first time, since the user is provisioned in OutSystems at this point and it still doesn't have any associated roles. You will need to configure the user roles after the user's first login.

    ![](../../../../../.gitbook/assets/okta-invalid-permissions-users.png)

    If the authentication is unsuccessful, double-check your configuration settings.

**Note:** If you're using an older version of OutSystems UI you will need to change the logout flow of your OutSystems applications, as described for the SAML 2.0 authentication method. Check [Change the Logout flow of your OutSystems applications](configure-saml.md#change-logout-flow) for more information.

## Troubleshooting OKTA authentication issues

Since the OKTA end-user authentication method is very similar to the SAML 2.0 one, you can troubleshoot them in the same way:

* Check the [SAML Message Logs page](configure-saml.md#logs) for detailed information on OKTA messages exchanged for end-user authentication.
* Use the same method for [accessing the Users application when you're locked out](configure-saml.md#locked-access) due to incorrect configuration settings in end-user authentication.

