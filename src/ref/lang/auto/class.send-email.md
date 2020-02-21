---
kinds: >-
  ServiceStudio.Model.Nodes+SendEmail+Kind,
  ServiceStudio.Model.ProcessNodes+SendEmailActivity+Kind
helpids: 0
---

# Send Email

Sends an email to one or more recipients.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| Name | Identifies an element in the scope where it is defined, like a screen, action, or module. | Yes |  |  |
| From | Email address of the sender. |  |  | Use the EmailAddressCreate built-in function to create an encoded value for the 'From' property.  The default sender is configured in the Email Configuration in Service Center. |
| To | One or more email addresses to send the email. Separate email addresses with a comma \(,\). | Yes |  | To handle Email addresses use the Email data type and Email built-in functions. |
| CC | One or more email addresses to send a carbon copy of the email. Separate email addresses with a comma \(,\). |  |  | To handle Email addresses use the Email data type and Email built-in functions. |
| BCC | One or more email addresses to send a blind carbon copy of the email. Separate email addresses with a comma \(,\). |  |  | To handle Email addresses use the Email data type and Email built-in functions. |
| Log Content | Set to Yes to store the email content in the email logs of the Platform Server. Check the email logs in Service Center. | Yes | No |  |
| Email | Email screen to be used as the body of the email to send. | Yes |  |  |
| Description | Text that documents the element. |  |  | This property is only available in process flows. |
| Label | Text displayed in the back-office when an instance of this Send Email activity is executed. |  |  | This property is only available in process flows. |

## Runtime Properties

| Name | Description | Read Only | Type | Observations |
| :--- | :--- | :--- | :--- | :--- |
| EmailId | Identifier of the sent email. |  |  |  |
| ActivityId | Identifier of the process activity instance at runtime. | Yes |  |  |

