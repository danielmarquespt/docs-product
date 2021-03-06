---
tags: support-Installation_Configuration
---

# Configure OutSystems to Send Emails

OutSystems allows [sending emails from your applications](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/logic/emails.md%3E). For this to work you need to configure the SMTP \(Simple Mail Transference Protocol\) server to use for sending the emails.

This is an environment-wide configuration, allowing you to choose a different email provider for each environment.

## Configure the SMTP Server

1. In the environment management console \(Service Center\), navigate to the **Administration** tab and click **Email**.
2. Fill-in the information about the SMTP server to use, and click **Save** for the changes to take effect.

![](../../.gitbook/assets/configure-outsystems-to-send-emails-1.png)

To check if the SMTP is properly configured, try sending an email from an existing application.

## Don't Send Emails When Testing

When developing and testing, you need to ensure that no email gets sent to your customers by accident.

To redirect all emails to a list of test users, check the **Redirect Emails to Test List**. Add the email addresses to redirect the emails to, in the **Test List Addresses** field.

![](../../.gitbook/assets/configure-outsystems-to-send-emails-2.png)

In this example, all emails sent from this environment are redirected to an internal mailing list, instead of their original address.

## Configure the Environment Hostname

To ensure the links in your emails point to the right environment, be sure to set the environment hostname.

Navigate to the **Administration** tab and click **Environment Configuration**. Set the **Hostname** field with the domain name you want your users to navigate to.

![](../../.gitbook/assets/configure-outsystems-to-send-emails-3.png)

