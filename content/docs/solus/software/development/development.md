---
title: "Development"
date: "2025-05-04T20:04:55+08:00"
lastmod: "2025-05-04T20:04:55+08:00"
draft: false
toc: true
weight: 10
params:
  index: false
---

{{% alert context="info" %}}

- This is not the official documentation of Solus. If you need help with Solus, go to https://help.getsol.us/
- This documentation was originally created for the Solus Project, for which I was a contributor. The Solus Project is the sole rights holder of this work. See the [License page](/docs/license) for more information.

{{% /alert %}}

---

Solus provides a stable foundation for creating, testing, and deploying applications.

You can install tools such as text editors, programming languages, compilers, and version control systems. Solus also supports containerization and virtualization technologies.

## Getting Started

If you want to compile and develop software using Solus, we recommend installing the `system.devel` component.

```bash
sudo eopkg install -c system.devel
```

The `system.devel` component installs libraries and packages for software development, such as `clang`, `gcc`, and `make`.
