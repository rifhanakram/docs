---
title: Install .NET Core on Linux RHEL 7 package manager - .NET Core
description: Use a package manager to install .NET Core SDK and runtime on RHEL 7.
author: thraka
ms.author: adegeo
ms.date: 03/17/2020
---

# RHEL 7 Package Manager - Install .NET Core

[!INCLUDE [package-manager-switcher](includes/package-manager-switcher.md)]

This article describes how to use a package manager to install .NET Core on RHEL 7.

[!INCLUDE [package-manager-intro-sdk-vs-runtime](includes/package-manager-intro-sdk-vs-runtime.md)]

## Register your Red Hat subscription

To install .NET Core from Red Hat on RHEL, you first need to register using the Red Hat Subscription Manager. If this hasn't been done on your system, or if you're unsure, see the [Red Hat Product Documentation for .NET Core](https://access.redhat.com/documentation/net_core/).

## Install the .NET Core SDK

After registering with the Subscription Manager, you're ready to install and enable the .NET Core SDK. In your terminal, run the following commands to enable the RHEL 7 dotnet channel and install.

```bash
subscription-manager repos --enable=rhel-7-server-dotnet-rpms
yum install rh-dotnet31 -y
scl enable rh-dotnet31 bash
```

## Install the ASP.NET Core Runtime

After registering with the Subscription Manager, you're ready to install and enable the ASP.NET Core Runtime. In your terminal, run the following commands.

```bash
subscription-manager repos --enable=rhel-7-server-dotnet-rpms
yum install rh-dotnet31-aspnetcore-runtime-3.1 -y
scl enable rh-dotnet31 bash
```

## Install the .NET Core Runtime

After registering with the Subscription Manager, you're ready to install and enable the .NET Core Runtime. In your terminal, run the following commands.

```bash
subscription-manager repos --enable=rhel-7-server-dotnet-rpms
yum install rh-dotnet31-dotnet-runtime-3.1 -y
scl enable rh-dotnet31 bash
```

## See also

- [Using .NET Core 3.1 on Red Hat Enterprise Linux 7](https://access.redhat.com/documentation/en-us/net_core/3.1/html/getting_started_guide/gs_install_dotnet)
