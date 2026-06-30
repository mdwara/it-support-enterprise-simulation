# Windows Administration Tools

**Document ID:** KB-0002

**Version:** 1.0

**Author:** Kutbul Wara

**Created:** June 30, 2026

**Classification:** Internal

**Applies To:** Windows 10 & Windows 11 Workstations

---

# Purpose

This knowledge base article provides an overview of the primary Windows administrative tools used by IT Support Specialists. These tools assist in diagnosing hardware, software, operating system, and user-related issues while supporting enterprise Windows environments.

---

# Task Manager

## Purpose

Task Manager provides real-time information about system performance, running applications, processes, startup applications, and resource utilization.

## Common Uses

- Monitor CPU, Memory, Disk, and GPU usage
- End unresponsive applications
- Review running processes
- Analyze startup applications
- Identify performance bottlenecks

## When to Use

Use Task Manager when:

- A computer is running slowly.
- An application is not responding.
- High CPU or memory usage is suspected.
- Startup performance needs to be analyzed.

---

# Device Manager

## Purpose

Device Manager displays all hardware installed on the computer and its current operational status.

## Common Uses

- Verify hardware detection
- Update device drivers
- Troubleshoot hardware failures
- Identify devices with missing or incorrect drivers

## When to Use

Use Device Manager when:

- Hardware is not functioning properly.
- A newly installed device is not recognized.
- Driver issues are suspected.
- Devices display warning or error icons.

---

# Event Viewer

## Purpose

Event Viewer records Windows system, application, and security events to assist with troubleshooting.

## Common Uses

- Investigate system crashes
- Review application failures
- Identify hardware or driver errors
- Analyze system warnings and critical events

## When to Use

Use Event Viewer when:

- Windows reports unexpected errors.
- The computer crashes or restarts unexpectedly.
- Applications repeatedly fail.
- Historical event information is needed.

---

# Windows Services

## Purpose

Windows Services are background processes that provide essential operating system functionality.

## Common Uses

- Verify service status
- Start or restart services
- Troubleshoot application functionality
- Configure startup behavior

### Examples

- Print Spooler
- DHCP Client
- Windows Update
- Windows Defender
- Windows Time

## When to Use

Use Services when:

- Printers stop working.
- Windows Update fails.
- Network services are unavailable.
- An application depends on a Windows service.

---

# System Configuration (msconfig)

## Purpose

System Configuration is used to troubleshoot startup and boot-related issues.

## Common Uses

- Configure startup options
- Select diagnostic startup modes
- Modify boot settings
- Troubleshoot software conflicts

## When to Use

Use System Configuration when:

- Windows fails to start normally.
- Startup troubleshooting is required.
- Safe Mode needs to be configured.
- Boot options need to be modified.

---

# Computer Management

## Purpose

Computer Management is a centralized administration console that combines multiple Windows management tools.

## Tools Included

- Device Manager
- Disk Management
- Event Viewer
- Shared Folders
- Local Users and Groups (Windows Pro/Enterprise)
- Services

## When to Use

Use Computer Management when:

- Managing local computer resources.
- Troubleshooting storage devices.
- Reviewing shared folders.
- Accessing multiple administrative tools from one location.

---

# Best Practices

- Gather information before making system changes.
- Verify the user's issue before troubleshooting.
- Document all findings and actions.
- Avoid making unnecessary configuration changes.
- Confirm the issue has been resolved before closing the support ticket.

---

# Related Windows Administrative Tools

| Tool | Command |
|------|---------|
| Task Manager | Ctrl + Shift + Esc |
| Device Manager | devmgmt.msc |
| Event Viewer | eventvwr.msc |
| Services | services.msc |
| System Configuration | msconfig |
| Computer Management | compmgmt.msc |
| System Information | msinfo32 |
| Disk Management | diskmgmt.msc |

---

# Summary

Windows administrative tools are essential resources for IT Support Specialists. Understanding when and how to use each tool enables technicians to diagnose issues efficiently, minimize downtime, and provide effective technical support. Familiarity with these tools improves troubleshooting accuracy and supports consistent, high-quality IT service.

---

# Related Knowledge Base Articles

- KB-0001 – Computer Hardware Overview
- HD-0001 – Slow Laptop
- HD-0002 – Printer Not Printing