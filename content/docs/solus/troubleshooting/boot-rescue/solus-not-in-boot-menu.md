---
title: "Solus does not appear in the startup menu"
icon: "sailing"
date: "2025-05-04T20:04:55+08:00"
lastmod: "2025-05-04T20:04:55+08:00"
draft: false
toc: true
weight: 30
params:
  index: false
---

{{% alert context="info" %}}

- This is not the official documentation of Solus. If you need help with Solus, go to https://help.getsol.us/
- This documentation was originally created for the Solus Project, for which I was a contributor. The Solus Project is the sole rights holder of this work. See the [License page](/docs/license) for more information.

{{% /alert %}}

---

## Cause

After a software update, Solus might disappear from the startup menu. This situation commonly occurs on systems using a legacy startup method (non-UEFI systems) where another Linux distribution owns the startup manager (such as GRUB).

## Procedure
- To restore access to Solus, access the other operating system and update the startup manager. 

  For more information, check the documentation of your distribution.