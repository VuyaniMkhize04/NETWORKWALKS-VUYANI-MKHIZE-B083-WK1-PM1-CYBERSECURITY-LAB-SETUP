# Kali Linux VirtualBox Cybersecurity Lab Setup

## 1. Project Overview

This project documents the setup and configuration of a Kali Linux virtual machine using Oracle VirtualBox on a Windows computer.

The objective was to establish a working Linux environment, configure its network settings, verify network connectivity, and create a snapshot to preserve the configured environment before proceeding with further cybersecurity exercises.

The project also documents the technical challenges encountered during setup, the troubleshooting approaches explored, and the lessons learned.

## 2. Objectives

- Install and configure Kali Linux in a virtualised environment.
- Configure IP and network settings in Kali Linux.
- Verify network connectivity.
- Troubleshoot network configuration and interface-navigation issues.
- Create a VirtualBox snapshot to preserve a working environment.
- Document the implementation process using screenshots.
- Record problems encountered, troubleshooting steps, and key learnings.

## 3. Lab Environment

| Component | Details |
|---|---|
| Host Operating System | Microsoft Windows |
| Virtualisation Platform | Oracle VirtualBox 7.2.22 |
| VirtualBox Build | r175245 |
| Guest Operating System | Kali Linux |
| Network Configuration | Configured and tested successfully |
| Recovery Point | VirtualBox snapshot |

## 4. Lab Setup and Implementation

### Step 1: Set Up the Virtual Machine

Kali Linux was configured to run as a virtual machine using Oracle VirtualBox.

Virtualisation provides an isolated environment for practising Linux administration, networking, and cybersecurity concepts without requiring a separate physical computer.

<img width="1917" height="1032" alt="Kali" src="https://github.com/user-attachments/assets/0d59f919-f14d-4118-9e3f-e046b7f1297b" />



### Step 2: Configure Network Settings

The network settings were configured within Kali Linux to establish network connectivity.

The configuration involved locating the network connection settings and editing the relevant IP configuration.

<img width="1027" height="691" alt="IP Configuration" src="https://github.com/user-attachments/assets/cfbe3f98-34b4-4d62-98b6-df1bbf2507d1" />


### Step 3: Verify Network Connectivity

After configuring the network settings, the connection was checked to confirm that networking was working.

The following Linux commands can be used to inspect network interfaces and IP addresses:

```bash
ip addr
```

To inspect routing information:

```bash
ip route
```

**Result:** Network connectivity was confirmed to be working after configuration.

<img width="1917" height="1025" alt="Network Checking" src="https://github.com/user-attachments/assets/0c1e3489-746f-476c-aa57-a283a5657e03" />


### Step 4: Shut Down the Virtual Machine

After completing the configuration and verifying connectivity, Kali Linux was shut down.

Shutting down the virtual machine provided an opportunity to save a recovery point of the configured environment.

### Step 5: Create a VirtualBox Snapshot

A snapshot was created in VirtualBox to preserve the configured state of the virtual machine.

**Snapshot name:** `Kali Linux – Initial Setup Complete`

**Description:** Kali Linux installed, network configuration completed, and connectivity verified.

The snapshot provides a recovery point that can be used if future changes during practical exercises cause configuration problems.

<img width="1720" height="1027" alt="Snapshot" src="https://github.com/user-attachments/assets/a9edab2f-1ac4-4f40-a213-be7cb7e682ae" />


## 5. Problems Encountered and Troubleshooting

### Problem 1: Microsoft Defender Could Not Scan Some Files

**Issue:**

During the VirtualBox setup process, Microsoft Defender reported that it could not scan some files.

**Troubleshooting approach:**

The scan warning was identified for further investigation before making changes to Windows security settings.

**Security consideration:**

Microsoft Defender should not be disabled simply to bypass a scan warning. The installer source and any threat detection details should be checked before allowing or restoring files.

**Outcome:**

The warning was encountered, but its final resolution was not confirmed as part of this lab.

### Problem 2: Network Manager Was Not Visible in VirtualBox

**Issue:**

The network-management option shown in the tutorial could not initially be located under the VirtualBox File and Tools menus.

**Environment:**

Oracle VirtualBox 7.2.22 (r175245).

**Troubleshooting approach:**

The installed VirtualBox version was checked, and the available network-management options were investigated.

**Lesson learned:**

Software versions can have different interface layouts, so instructions shown in a tutorial may not match the installed version exactly.

The required network configuration was subsequently completed through Kali Linux.

### Problem 3: The "Edit Connections" Option Was Missing in Kali Linux

**Issue:**

The network connection editing option shown in the tutorial was not immediately visible in the Kali Linux interface.

**Troubleshooting approach:**

The network configuration interface was located, allowing the connection settings to be edited.

An alternative command for opening the NetworkManager connection editor is:

```bash
nm-connection-editor
```

To inspect network interfaces and their IP addresses, the following command can be used:

```bash
ip addr
```

**Outcome:**

The IP configuration was completed successfully, and network connectivity was confirmed to be working.

**Lesson learned:**

Understanding both graphical network-management tools and Linux terminal commands makes it easier to troubleshoot configuration issues.

## 6. Results

The following outcomes were achieved:

- Kali Linux was configured to run in Oracle VirtualBox.
- Network and IP settings were configured.
- Network connectivity was verified as working.
- A VirtualBox snapshot was created to preserve the configured environment.
- Troubleshooting experiences and technical lessons were documented.

## 7. Key Learnings

This exercise provided practical exposure to:

- Linux virtualisation using Oracle VirtualBox.
- IP address and network configuration.
- Linux network inspection commands.
- Troubleshooting differences between tutorial instructions and software interfaces.
- Network connectivity verification.
- Virtual machine snapshots and recovery points.
- Technical documentation and problem-solving.

## 8. Security Considerations

- Verify software download sources before installation.
- Investigate antivirus warnings rather than automatically bypassing them.
- Avoid exposing passwords, access tokens, and sensitive network information in screenshots.
- Create recovery points before making significant changes to a virtual machine.
- Use cybersecurity tools only on systems and networks for which you have permission.

## 9. Future Improvements

As I continue developing my cybersecurity skills, I plan to extend my practical experience through:

- Linux command-line exercises.
- Networking fundamentals and troubleshooting.
- Network scanning in authorised lab environments.
- Security log analysis.
- Security monitoring and SIEM exercises.

Completed exercises will be documented separately with their own objectives, procedures, screenshots, and results.

## 10. Conclusion

This project established a working Kali Linux environment in Oracle VirtualBox, with successful network configuration and a saved snapshot.

The setup process also provided experience in troubleshooting technical issues, adapting to differences in software interfaces, and documenting practical work.

This lab serves as a foundation for further hands-on learning in Linux, networking, and cybersecurity.

## Author

**Vuyani Mkhize**

Cybersecurity learner | ICT Applications Development student

