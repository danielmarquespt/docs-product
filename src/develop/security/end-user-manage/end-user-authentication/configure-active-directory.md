---
summary: >-
  How to configure Active Directory end-user authentication for your
  applications.
---

# Configure Active Directory Authentication

 Only available in OutSystems on-premises installations.

The Active Directory authentication method for authenticating end-users requires the front-end server to be part of the Active Directory domain.

To use Active Directory domain authentication:

1. In the [Users application](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/security/end-user-manage/accessing-users.md%3E), click "Configure Authentication" in the sidebar.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/security/end-user-manage/end-user-authentication/images/users-auth-active-directory.png%3E)

2. Choose `Active Directory` in the **Authentication** drop-down list.
3. Add the authentication domain in the **Default Domain** text field.
4. To enable Integrated Windows Authentication for all applications, select **Windows Integrated Authentication**.

   Alternatively, you can enable Integrated Windows Authentication for a just [a selected number of elements](integrated-authentication.md) in Service Studio \(e.g. just for some web screens, web flows or web services\).

