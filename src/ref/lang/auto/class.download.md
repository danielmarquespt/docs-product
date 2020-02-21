---
kinds: >-
  ServiceStudio.Model.Nodes+Download+Kind,
  ServiceStudio.Model.NRNodes+Download+Kind
helpids: 0
---

# Download

Sends a file to the user.  
Triggers an action for the browser to download the file.

## Properties

| Name | Description | Mandatory | Default value | Observations |
| :--- | :--- | :--- | :--- | :--- |
| File Content | Holds the file selected by the user. | Yes |  |  |
| File Name | Text literal or expression with the name of the file, including the extension. | Yes |  |  |
| Mime-Type | Text literal or expression specifying the media type of the file. | Yes | "application/octet-stream" | Example values:  – "application/x-msexcel";  – "application/msword";  – "application/pdf";  – "image/gif";  – "text/html";  – "video/avi";  – "audio/wav". |
| Save to Disk | Set to Yes to allow the user to open or save the file. | Yes | Yes |  |

