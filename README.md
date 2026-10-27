# Kali Linux VirtualBox Cybersecurity Lab Setup

> A practical lab documenting the setup of Kali Linux in Oracle
> VirtualBox, network configuration, troubleshooting, and snapshot
> creation.

## Table of Contents

-   [1. Project Overview](#1-project-overview)
-   [2. Objectives](#2-objectives)
-   [3. Lab Environment](#3-lab-environment)
-   [4. Setup and Implementation](#4-setup-and-implementation)
-   [5. Problems Encountered and
    Troubleshooting](#5-problems-encountered-and-troubleshooting)
-   [6. Results](#6-results)
-   [7. Key Learnings](#7-key-learnings)
-   [8. Security Considerations](#8-security-considerations)
-   [9. Future Improvements](#9-future-improvements)
-   [10. Conclusion](#10-conclusion)
-   [Author](#author)

------------------------------------------------------------------------

## 1. Project Overview

This project documents the setup and configuration of a Kali Linux
virtual machine using Oracle VirtualBox on a Windows computer.

The objective was to establish a working Linux environment, configure
its network settings, verify network connectivity, and create a snapshot
to preserve the configured environment before proceeding with further
cybersecurity exercises.

This documentation also records the technical challenges encountered
during setup, the troubleshooting approaches explored, and the lessons
learned.

## 2. Objectives

-   Set up Kali Linux in a virtualised environment.
-   Configure IP and network settings in Kali Linux.
-   Verify network connectivity.
-   Troubleshoot network configuration and interface-navigation issues.
-   Create a VirtualBox snapshot to preserve a working environment.
-   Document the implementation process with screenshots.
-   Record problems encountered, troubleshooting approaches, and key
    learnings.

## 3. Lab Environment

  Component                 Details
  ------------------------- ----------------------------------------------
  Host operating system     Microsoft Windows
  Virtualisation platform   Oracle VirtualBox 7.2.22
  VirtualBox build          r175245
  Guest operating system    Kali Linux
  Network configuration     Configured; connectivity reported as working
  Recovery point            VirtualBox snapshot

## 4. Setup and Implementation

### Step 1: Set Up the Virtual Machine

Kali Linux was set up to run as a virtual machine using Oracle
VirtualBox.

Virtualisation provides an environment for practising Linux
administration, networking, and cybersecurity concepts without requiring
a separate physical computer.

**Screenshot:** Add a screenshot of the Kali Linux virtual machine in
VirtualBox.

![Kali Linux virtual machine](screenshots/01-virtualbox-kali-vm.png)

### Step 2: Configure Network Settings

The network settings were configured within Kali Linux to establish
network connectivity. The network connection settings were located, and
the relevant IP configuration was edited.

**Screenshot:** Add a screenshot of your network configuration. Hide
sensitive information before uploading.

![Kali Linux network settings](screenshots/02-kali-network-settings.png)

### Step 3: Verify Network Connectivity

After configuring the network settings, connectivity was checked and
reported to be working.

The following commands can be used to inspect network interfaces and IP
addresses:

``` bash
ip addr
```

To inspect routing information:

``` bash
ip route
```

These commands are included as useful reference commands. Only describe
them as tests you performed if you actually ran them.

**Result:** Network connectivity was confirmed to be working after
configuration.

**Screenshot:** Add a screenshot of your actual successful connectivity
test, if you captured one.

![Network connectivity
verification](screenshots/03-network-connectivity.png)

### Step 4: Shut Down the Virtual Machine

After completing the configuration, Kali Linux was shut down.

### Step 5: Create a VirtualBox Snapshot

A snapshot was created in VirtualBox to preserve the configured state of
the virtual machine.

**Snapshot name:** `Kali Linux – Initial Setup Complete`

**Description:** Kali Linux setup completed, network configuration
completed, and connectivity verified.

The snapshot provides a recovery point that can be used if future
changes during practical exercises cause configuration problems. A
snapshot is useful, but it is not a replacement for an independent
backup.

**Screenshot:** Add a screenshot showing the snapshot in the VirtualBox
Snapshots interface.

![VirtualBox snapshot](screenshots/04-virtualbox-snapshot.png)

## 5. Problems Encountered and Troubleshooting

### Problem 1: Microsoft Defender Could Not Scan Some Files

**Issue**

During the VirtualBox setup process, Microsoft Defender reported that it
could not scan some files.

**Troubleshooting and security considerations**

The warning should be investigated before changing Windows security
settings. Check that the installer came from the official VirtualBox
website and review Windows Security's Protection History for the exact
message or any threat detection.

Do not disable Microsoft Defender or allow a flagged file simply to
bypass the warning.

**Outcome**

The scan warning was encountered, but its final resolution was not
confirmed during this lab. Update this section if you later verify how
it was resolved.

### Problem 2: Network Manager Was Not Visible in VirtualBox

**Issue**

The network-management option shown in the tutorial could not initially
be located under the VirtualBox **File → Tools** menu.

**Environment**

Oracle VirtualBox 7.2.22 (r175245).

**Troubleshooting approach**

The installed VirtualBox version was checked, and the available
network-management options were investigated. The required network
configuration was subsequently completed through Kali Linux.

**Lesson learned**

Software versions can have different interface layouts, so tutorial
instructions may not match the installed version exactly. It is
important to check the version and identify the correct settings for the
environment being used.

### Problem 3: The "Edit Connections" Option Was Missing in Kali Linux

**Issue**

The network connection editing option shown in the tutorial was not
immediately visible in the Kali Linux interface.

**Troubleshooting approach**

The network configuration interface was located, allowing the connection
settings to be edited. If installed, the NetworkManager connection
editor can also be opened from a terminal using:

``` bash
nm-connection-editor
```

To inspect network interfaces and their IP addresses, use:

``` bash
ip addr
```

To inspect the routing table, use:

``` bash
ip route
```

**Outcome**

The IP configuration was completed successfully, and network
connectivity was reported to be working.

**Lesson learned**

Knowing both graphical network-management tools and Linux terminal
commands provides alternative ways to investigate networking issues.

## 6. Results

The following outcomes were achieved during this setup:

-   Kali Linux was configured to run in Oracle VirtualBox.
-   Network and IP settings were configured.
-   Network connectivity was reported to be working.
-   A VirtualBox snapshot was created to preserve the configured
    environment.
-   The troubleshooting process and technical lessons were documented.

## 7. Key Learnings

This exercise provided practical exposure to:

-   Linux virtualisation using Oracle VirtualBox.
-   IP address and network configuration.
-   Linux network inspection commands.
-   Troubleshooting differences between tutorial instructions and
    software interfaces.
-   Network connectivity verification.
-   Virtual machine snapshots and recovery points.
-   Technical documentation and problem-solving.

## 8. Security Considerations

-   Verify software download sources before installation.
-   Investigate antivirus warnings rather than automatically bypassing
    them.
-   Do not publish passwords, access tokens, personal files, or
    sensitive network details in screenshots.
-   Create recovery points before making significant changes to a
    virtual machine.
-   Use cybersecurity tools only on systems and networks for which you
    have permission.
-   Remember that a VirtualBox snapshot is not a substitute for an
    independent backup.

## 9. Future Improvements

As I continue developing my cybersecurity skills, I plan to expand my
practical experience through:

-   Linux command-line exercises.
-   Networking fundamentals and troubleshooting.
-   Network scanning in authorised lab environments.
-   Security log analysis.
-   Security monitoring and SIEM exercises.

Future exercises can be documented with their own objectives,
procedures, screenshots, and verified results.

## 10. Conclusion

This project established a Kali Linux environment in Oracle VirtualBox,
with network configuration completed and a snapshot created.

The setup process also provided experience in troubleshooting technical
issues, adapting to differences in software interfaces, and documenting
practical work.

This lab serves as a foundation for further hands-on learning in Linux,
networking, and cybersecurity.

## Author

**Vuyani Mkhize**

ICT Applications Development student \| Cybersecurity learner

------------------------------------------------------------------------

## Screenshot Checklist

Before publishing, add your own screenshots to the `screenshots` folder
and make sure their filenames match the image links used above:

-   `01-virtualbox-kali-vm.png` --- Kali Linux virtual machine in
    VirtualBox.
-   `02-kali-network-settings.png` --- Kali Linux network settings.
-   `03-network-connectivity.png` --- Actual connectivity test, if
    captured.
-   `04-virtualbox-snapshot.png` --- Created VirtualBox snapshot.

If you do not have a screenshot for a section, remove that image link
until you can add the correct screenshot. Do not use example images as
evidence of your own work.
