---
kinds: ServiceStudio.Model.ESpace+Kind
helpids: 1011
---

# Module

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies the module. | Yes |  |  |
| Description | Text that documents the element. |  |  | Useful for documentation purpose. The maximum size of this property is 2000 characters. |
| DBMS | Defines the DataBase Management System type considered by developers when writing SQL. The development environment executes some validations regarding your queries regarding compliance with the selected DBMS. | Yes | \(All\) | The possible values are: Oracle, SqlServer, \(All\).  This property allows the development environment to execute some validations on SQL queries to check if the SQL is compliant with the DBMS type specified in this property.  It must be set according to the OutSystems Platform Server Database, otherwise a warning message is presented and you should either specify the exact database type or select \(All\).  Though this property is merely informative, it is important for communication and knowledge transfer between developers. |
| Is User Provider | Set to Yes to make this a module which provides users. | Yes | No | When this property is set to Yes, the Users entity \(System\) is set as public and the module becomes available as an option as a user source in modules User Provider Module property. |
| User Provider module | Specifies a source for the user records to be used by this module. |  | Users | By default it shows the following possible values: \(Current eSpace\), ServiceCenter, Users. |
| Icon | Identifies the module in the element tree of the development environment. | Yes | Default Icon | The module icon is also displayed in the "Manage Dependencies" dialog box. |
| Web |  |  |  |  |
| Default Theme | Main theme defining the look and feel to apply to the screens and blocks of the module. |  |  |  |
| jQuery Version | jQuery version used in all screens and blocks of the module. | Yes | 1.8.3 | The possible values are: 1.8.3, 1.4.2 OS \(Note: this older jQuery version is being deprecated\). |
| Global Exception Handler | Specifies the 'OnException' handler to be used by all the flows of this module. |  | Common\OnException |  |
| JavaScript | JavaScript associated with this element. |  |  | Click on "..." to edit the property value. |
| Validation Messages |  |  |  |  |
| Mandatory Input | Default message displayed whenever a mandatory input field is left empty. |  | "Required field!" |  |
| Invalid Integer | Default message displayed whenever a provided value is not of Integer type as expected by an input field. |  | "Integer expected!" |  |
| Invalid Decimal | Default message displayed whenever a provided value is not of Decimal type as expected by an input field. |  | "Decimal expected!" |  |
| Invalid Currency | Default message displayed whenever a provided value is not of Currency type as expected by an input field. |  | "Currency expected!" |  |
| Invalid Date | Default message displayed whenever a provided value is not of Date type as expected by an input field. |  | "Date expected!" |  |
| Invalid Time | Default message displayed whenever a provided value is not of Time type as expected by an input field. |  | "Time expected!" |  |
| Invalid DateTime | Default message displayed whenever a provided value is not of DateTime type as expected by an input field. |  | "DateTime expected!" |  |
| Invalid Text | Default message displayed whenever a provided value is not of Text type as expected by an input field. |  | "Text expected!" |  |
| Invalid Phone | Default message displayed whenever a provided value is not of Phone type as expected by an input field. |  | "Phone Number expected!" |  |
| Invalid Numeric Password | Default message displayed whenever a provided value is not of Numberic Password type as expected by an input field. |  | "Numeric Password expected!" |  |
| Invalid Email | Default message displayed whenever a provided value is not of Email type as expected by an input field. |  | "Email expected!" |  |
| Upgrade Messages |  |  |  |  |
| Upgrade Complete |  |  | "Your application has been updated to the latest version." |  |
| Upgrade Failed |  |  | "An error occurred while trying to update the app. If you want to retry the update, restart the app." |  |
| Upgrade Failed on Resources |  |  | "An error occurred while trying to update the app. If you want to retry the update, restart the app." |  |
| Upgrade Failed on Data Model |  |  | "An error occurred while trying to update the app. If you want to retry the update, restart the app. If the problem persists you can reinstall, but all local data will be lost." |  |
| Upgrade Required |  |  | "Your application needs to be updated. Tap here to update." |  |
| Upgrade Required with Data Loss |  |  | "Your application needs to be updated. Unsaved data will be lost. Tap here to update." |  |
| Advanced |  |  |  |  |
| Use Cookies | Set to Yes to use cookies to exchange the session identifier through the Web Browser cookies. If set to No, the session identifier is sent back and forth in the URL. | Yes | Yes |  |
| Is Multi-tenant | Set to Yes to enable multi-tenancy for this module. | Yes | No |  |
| Web Screen Rendering Mode | Defines the DOCTYPE declaration to put in generated HTML pages. | Yes | HTML 5 | The possible values are: HTML 5, XHTML Transitional, Quirks. |
| Web Services Namespace | Namespace of the WSDL generated by this module. |  |  |  |

