---
title: "Java"
date: "2025-05-04T20:04:55+08:00"
lastmod: "2025-05-04T20:04:55+08:00"
draft: false
toc: true
weight: 225
params:
  index: false
---

{{% alert context="info" %}}

- This is not the official documentation of Solus. If you need help with Solus, go to https://help.getsol.us/
- This documentation was originally created for the Solus Project, for which I was a contributor. The Solus Project is the sole rights holder of this work. See the [License page](/docs/license) for more information.

{{% /alert %}}

---

Solus includes multiple LTS versions of Java in the repositories. You can install more than one version in your system at once.

{{< alert context="info" text="If you need to install different versions or Java, use alternative installation methods such as [_SDKMAN!_](https://sdkman.io/)." />}}

All Java packages in the Solus repositories include the _Java Runtime Environment_ (JRE) and the _Java Development Kit_ (JDK).

The following table lists the versions of Java available in the Solus repositories.

| Version | Package name | Installation directory  | Included components | Notes |
| ------- | ------------ | ----------------------- | ------------------- | ----- |
| Java 11 | `openjdk-11` | `/usr/lib64/openjdk-11` | JRE, JDK, OpenJFX   |       |
| Java 17 | `openjdk-17` | `/usr/lib64/openjdk-17` | JRE, JDK            |       |
| Java 21 | `openjdk-21` | `/usr/lib64/openjdk-21` | JRE, JDK            |       |

## Running Java applications

{{< alert context="warning" text="Solus does not add Java to the `PATH` environment variable by default." />}}

There are multiple ways to execute Java applications in Solus:

- Create a .desktop file, then add `env JAVA_HOME=/path/to/jdk/bin` to Exec.
- Create a script that sets `JAVA_HOME` before running the application.
- Symlink the `java` executable from `/path/to/jdk/bin` to `/usr/bin`.
- Add `/path/to/jdk/bin` to your PATH environment variable.
