# Day 2 Lab – Windows Administration & Troubleshooting

**Lab ID:** LAB-0002

**Date:** June 30, 2026

**Technician:** Kutbul Wara

**Department:** Information Technology

---

# Objective

The objective of this lab was to become familiar with essential Windows administrative tools used by IT Support Specialists to troubleshoot operating system, hardware, and software issues. The lab focused on Windows Services, Event Viewer, Startup Applications, System Configuration, and Computer Management.

---

# Lab 1 – Windows Services

## Tool Used

- Services (services.msc)

## Information Collected

| Service | Status | Startup Type |
|---------|--------|--------------|
| DHCP Client | Running | Automatic |
| Print Spooler | Running | Automatic |
| Windows Update | Stopped | Manual |

### Observations

- DHCP Client was running automatically, allowing the computer to receive network configuration from a DHCP server.
- Print Spooler was running correctly, indicating that printing services were available.
- Windows Update was stopped with a Manual startup type, which is normal because Windows starts this service only when updates are required.

### Screenshot

`images/day-02/services.png`

---

# Lab 2 – Event Viewer

## Tool Used

- Event Viewer (eventvwr.msc)

### Warning Event

| Field | Value |
|------|------|
| Date | June 30, 2026 – 12:42 PM |
| Log | System |
| Source | e1dexpress |
| Event ID | 27 |

**Description**

The Intel Ethernet adapter reported that the network cable or connection was disconnected. This warning commonly appears when an Ethernet cable is unplugged or the system is connected using Wi-Fi instead of a wired network.

---

### Error Event

| Field | Value |
|------|------|
| Date | June 30, 2026 – 12:19 PM |
| Log | System |
| Source | NDIS |
| Event ID | 10317 |

**Description**

The Microsoft Wi-Fi Direct Virtual Adapter experienced a power transition failure while attempting to enter an operational state. This event typically relates to virtual wireless adapters and does not always indicate a user-impacting problem.

### Observations

- Event Viewer records both informational and diagnostic events that assist IT technicians during troubleshooting.
- Not every warning or error requires immediate action. Understanding the context of an event is essential before determining whether it affects the user.

### Screenshot

`images/day-02/event-viewer.png`

---

# Lab 3 – Startup Applications

## Tool Used

- Task Manager → Startup Apps

### Information Collected

| Item | Value |
|------|------|
| Enabled Startup Applications | 8 |
| Highest Startup Impact | RtkAudUService64, SecurityHealthSystray |
| Applications That Could Be Disabled | WhatsApp, Microsoft Edge |

### Observations

- Eight applications were configured to launch automatically when Windows starts.
- Some applications are essential for Windows security and hardware functionality, while others are optional and may increase startup time.
- Disabling unnecessary startup applications can improve boot performance.

### Screenshot

`images/day-02/startup-apps.png`

---

# Lab 4 – System Configuration

## Tool Used

- System Configuration (msconfig)

### Information Collected

| Item | Value |
|------|------|
| Startup Selection | Normal Startup |
| Boot Option | Windows 11 (C:\Windows): Current OS; Default OS |

### Observations

- The computer is configured to start normally using all device drivers and Windows services.
- System Configuration can be used to troubleshoot startup issues by enabling Selective Startup or modifying boot options.

### Screenshot

`images/day-02/msconfig.png`

---

# Lab 5 – Computer Management

## Tool Used

- Computer Management (compmgmt.msc)

### Areas Reviewed

- Device Manager
- Disk Management
- Computer Management Console

### Observations

- Computer Management provides centralized access to multiple Windows administrative tools.
- Device Manager allows technicians to identify hardware and driver issues.
- Disk Management provides information about storage devices, partitions, and drive health.
- Local Users and Groups was not available because the system is running Windows 11 Home.

### Screenshots

- `images/day-02/computer-management.png`
- `images/day-02/disk-management.png`

---

# Lessons Learned

- Windows administrative tools provide valuable information for diagnosing hardware, software, and operating system issues.
- Services should always be checked when troubleshooting functionality such as printing or networking.
- Event Viewer helps identify historical system events and should be used to investigate recurring problems.
- Startup applications can significantly affect boot performance.
- Computer Management provides centralized access to many commonly used administrative tools.

---

# Conclusion

This lab provided hands-on experience using several Windows administrative tools commonly used by IT Support Specialists. By exploring Services, Event Viewer, Startup Applications, System Configuration, and Computer Management, I gained a better understanding of how Windows components work together and how these tools assist in diagnosing and resolving user issues. These skills will support future troubleshooting activities and improve efficiency when responding to help desk tickets.
