---
summary: >-
  How to configure LDAP end-user authentication for your applications (both LDAP
  with Active Directory and standard LDAP).
---

# Configure LDAP Authentication

There are two ways of configuring LDAP \(Lightweight Directory Access Protocol\) for authenticating end-users of your OutSystems applications:

Use LDAP protocol to connect to Active Directory \(AD\) : Used when you have an Active Directory infrastructure that you want to connect to, but the OutSystems front-end servers cannot be part of the Active Directory domain \(e.g. in cloud infrastructures\). Use this option for a simplified configuration process. Note that the front-end servers must be able to access the Active Directory domain controller.

Use standard LDAP : Used when you are connecting to a non-AD infrastructure like OpenLDAP.

## Configure LDAP Authentication with Active Directory

To configure the OutSystems end-user authentication for LDAP with Active Directory do the following:

1. In the [Users application](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/security/end-user-manage/accessing-users.md%3E), click "Configure Authentication" in the sidebar.
2. Choose `LDAP` in the **Authentication** drop-down list.
3. In the **LDAP URL** field, enter the URL in the following format:

   `ldap://<LDAP_Server>:<Port>/<Base_Distinguished_Name>`

   Check [Obtain Active Directory configuration information](configure-ldap.md#obtain-ad-info%3E) for more information on how you can build this field value.

   _Notes:_  
   To use secure LDAP, use the protocol `ldaps://` instead.  
   The `ldap://` prefix can be omitted in the URL, but you must include the `ldaps://` prefix when using secure LDAP.

4. Select **Use AD credentials**.

   ![](../../../../../.gitbook/assets/users-auth-ldap-ad.png)

5. Optionally, in the **Default Domain** field, enter the domain where end-users are going to be authenticated.
6. Test your configurations by entering your credentials in the respective fields for testing:

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/security/end-user-manage/end-user-authentication/images/users-auth-test-configuration.png%3E)

### Example

Consider the following example where we are using the ADSI Edit tool, included in [Windows Remote Server Administration Tools \(RSAT\)](https://support.microsoft.com/en-us/help/2693643/remote-server-administration-tools-rsat-for-windows-operating-systems>), to explore the Active Directory hierarchy tree.

In this case the domain controller address \(which we will use as our server address\) is `DOMAINCONTROLLER.domain.outsystems.com`, configured in the default port, and the Distinguished Name \(DN\) of the displayed root LDAP node is `DC=domain,DC=outsystems,DC=com`.

![](../../../../../.gitbook/assets/adsi-domaincontroller.png)

If we wanted to authenticate end-users configured under the `CN=Users` LDAP node we would use the following Base Distinguished Name in the LDAP URL field:

`CN=Users,DC=domain,DC=outsystems,DC=com`

Note that Distinguished Names are read from right \(root\) to left \(leaf\). The final value of the **LDAP URL** field would be:

`ldap://DOMAINCONTROLLER.domain.outsystems.com/CN=Users,DC=domain,DC=outsystems,DC=com`

## Configure Standard LDAP Authentication

To configure OutSystems end-user authentication with standard LDAP \(i.e. LDAP not associated with Active Directory\) do the following:

1. Choose `LDAP` in the **Authentication** drop-down list.
2. In the **LDAP URL** field, enter the URL in the following format:

   `ldap://<LDAP_Server>:<Port>/<Base_Distinguished_Name>`.

   _Notes:_  
   To use secure LDAP, use the `ldaps://` URL scheme instead.  
   The `ldap://` prefix can be omitted in the URL, but you must include the `ldaps://` prefix when using secure LDAP.

3. Select **Use Standard LDAP**.
4. In **User Search Filter** write the filter to use when searching users. The `{0}` placeholder denotes the username. If no query is defined, the username will be sent to the LDAP server exactly as it was provided.

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/security/end-user-manage/end-user-authentication/images/ldap-user-search-filter.png%3E)

   OutSystems provides a few search filter examples in the help text below the **User Search Filter** field. For more information on search filters check the [Search Filter Syntax](https://docs.microsoft.com/en-us/windows/desktop/adsi/search-filter-syntax>) in Microsoft's documentation.

   You can use a tool like Microsoft's [Active Directory Explorer](https://docs.microsoft.com/en-us/sysinternals/downloads/adexplorer>) to explore the information stored in your LDAP provider, and to build and test your search filters. Note that if your LDAP server does not allow unauthenticated operations, you will need to provide user credentials for a user with permissions to perform search operations.

   **Note:** Some LDAP servers, especially non-AD ones, only allow you to login with the **LDAP Distinguished Name \(DN\)** of the user. Using a search filter allows the platform to take an OutSystems username and search for its distinguished name in the LDAP server before attempting to log in the user.

5. Test your configurations by entering your credentials in the respective fields for testing:

![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/security/end-user-manage/end-user-authentication/images/users-auth-test-configuration.png%3E)

## Obtain Active Directory Configuration Information { \#obtain-ad-info }

### Using a computer which is part of the Active Directory

If you are using a computer that **is part of the Active Directory domain** you wish to use for authenticating end-users, you can use tools available out-of-the-box in Windows to find the necessary information \(domain name, Base Distinguished Name and domain controller address\) to build the **LDAP URL** field value.

1. **Obtain your current domain name.**

   If you're using Windows 8 or higher, open the **Settings** app and then go to Accounts &gt; "Access work or school". There will be an indication telling you that you are connected to an Active Directory domain and what is its domain name:

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/security/end-user-manage/end-user-authentication/images/domain-howto-win10.png%3E)

   If using Windows 7, open **Control Panel**, go to **System and Security** and click on System. The current domain is shown in the "Computer name, domain and workgroup settings".

   ![](https://github.com/danielmarquespt/docs-product/tree/e7ea3f444d5129dab245c69ab72ae091554bc4fb/src/develop/security/end-user-manage/end-user-authentication/images/domain-howto-win7.png%3E)

2. **Get the Base Distinguished Name from the domain name.**

   Apply the following transformation to build it from the domain name:

   1. Replace any `"."` \(dot\) character in the domain address with a `","` \(comma\) character.  
   2. Add `DC=` before each part of the address.

      For example, `domain.outsystems.com` becomes `DC=domain,DC=outsystems,DC=com`.

      _Tip:_ You can narrow down the LDAP search by providing a more specific Base Distinguished Name \(BDN\). In the following example we added another part to the BDN so that we only authenticate users configured under the `CN=Users` LDAP node:

      `CN=Users,DC=domain,DC=outsystems,DC=com`

3. **Obtain the LDAP server address \(in this case, the AD Domain Controller server address\).**

   There are several ways of getting this information. Here's two possible ways:

   **A\)** Open a command-line console and run the `nslookup` command. You will get a `>` prompt where you should execute the following commands, replacing `DOMAINNAME.mycompany.com` with your specific domain name:

   `set type=all`  
   `_ldap._tcp.dc._msdcs.DOMAINNAME.mycompany.com`

   The second command will output some information. Search for any lines in the form:

   `svr hostname = SERVERNAME.mycompany.com`

   These are addresses for Active Directory domain controllers. Choose one of the server addresses to include in the **LDAP URL** field.  
   For more information check [How to verify that SRV DNS records have been created for a domain controller](https://support.microsoft.com/en-us/help/816587/how-to-verify-that-srv-dns-records-have-been-created-for-a-domain-cont>) in Microsoft's documentation.

   _Tip:_ If you get more than one address, check with your network administrator which is the most appropriate one.

   **B\)** Alternatively, open a command-line console and run the following command, replacing `DOMAINNAME.mycompany.com` with your own domain name:

   `nltest /dclist:DOMAINNAME.mycompany.com`

   You should get a list of Active Directory domain controller addresses \(one or more entries\), along with other information in each line. Choose one of the server addresses to include in the **LDAP URL** field.

   _Tip:_ If you get more than one address, check with your network administrator which is the most appropriate one.

### Using a computer outside of the Active Directory

If you are using a computer that **is not part of the Active Directory domain** you want to use for end-user authentication, ask your network administrator for the correct LDAP server address and Base Distinguished Name.

