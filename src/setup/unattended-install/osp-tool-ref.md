---
summary: Complete reference for the Solution Pack Tool (OSPTool) command line.
tags: >-
  support-Installation_Configuration;
  support-Installation_Configuration-overview
---

# Solution Pack Tool \(OSPTool\) Command Line Reference

 This article applies to: \*\*OutSystems 11\*\*  Other versions available: \[10\]\(https://success.outsystems.com/Documentation/10/Setting\_Up\_OutSystems/Unattended\_Installation\_and\_Upgrade/Solution\_Pack\_Tool\_\(OSPTool\)\_Command\_Line\_Reference\)

The Solution Pack Tool \(OSPTool\) allows you to publish OutSystems solutions on an environment.

The default path of the Solution Pack Tool command line is the following:

```text
C:\Program Files\Common Files\OutSystems\<version>\OSPTool.com
```

The Solution Pack Tool command line returns non-zero values when an error occurs.

## Syntax

```text
OSPTool.com /Publish {<osp_file>|<oap_file>} <hostname> <username> <password>
    | /PublishFactory <hostname> <username> <password>
```

## Parameters

`/Publish {<osp_file>|<oap_file>} <hostname> <username> <password>`

: Publishes the specified OutSystems Solution Pack \(`.osp`\) or OutSystems Application Pack \(`.oap`\) file.

`/PublishFactory <hostname> <username> <password>`

: Publishes all non-system components in the Environment specified by hostname. This helps to apply patch updates.

## Example

Publish an OutSystems Solution Pack \(`file.osp`\) file:

```text
OSPTool.com /Publish "file.osp" <hostname> <username> <password>
```

Publish an entire factory:

```text
OSPTool.com /PublishFactory <hostname> <username> <password>
```

