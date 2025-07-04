---
title: Basics of package management in Solus
date: "2025-05-04T20:04:55+08:00"
lastmod: "2025-05-04T20:04:55+08:00"
draft: false
toc: true
weight: 219
params:
  index: false
---

{{% alert context="info" %}}

- This is not the official documentation of Solus. If you need help with Solus, go to https://help.getsol.us/
- This documentation was originally created for the Solus Project, for which I was a contributor. The Solus Project is the sole rights holder of this work. See the [License page](/docs/license) for more information.

{{% /alert %}}

---

Solus uses the eopkg package manager. You can use `eopkg` to install, update, and remove software packages on your Solus system.

The following table lists the most common `eopkg` commands:

| Action                                                      | Command                                       | Example                                                      |
| ----------------------------------------------------------- | --------------------------------------------- | ------------------------------------------------------------ |
| Install software                                            | `sudo eopkg install PACKAGE_NAME`             | `sudo eopkg install gnome-documents gnome-music`             |
| Reinstall software                                          | `sudo eopkg install --reinstall PACKAGE_NAME` | `sudo eopkg install --reinstall gnome-documents gnome-music` |
| Uninstall software                                          | `sudo eopkg remove PACKAGE_NAME`              | `sudo eopkg remove gnome-documents gnome-music`              |
| Update your system                                          | `sudo eopkg upgrade`                          | -                                                            |
| Update specific software                                    | `sudo eopkg upgrade PACKAGE_NAME`             | `sudo eopkg upgrade firefox`                                 |
| Search for software                                         | `eopkg search KEYWORD`                        | `eopkg search documents`                                     |
| Get information on software, such as description or version | `eopkg info PACKAGE_NAME`                     | `eopkg info gnome-documents`                                 |
