# Networking Fundamentals

**Document ID:** KB-0003

**Version:** 1.0

**Author:** Kutbul Wara

**Created:** July 1, 2026

**Classification:** Internal

**Applies To:** Windows 10 & Windows 11 Workstations

---

# Quick Reference

| Issue | Recommended Tool |
|--------|------------------|
| No Internet Connection | `ipconfig` |
| Invalid IP Address | `ipconfig /renew` |
| Cannot Browse Websites | `nslookup` |
| Slow Network Connection | `ping` |
| Unable to Reach Remote Server | `tracert` |
| Verify Full Network Configuration | `ipconfig /all` |

---

# Purpose

This knowledge base article explains the fundamental networking concepts and Windows networking tools used by IT Support Specialists to diagnose and resolve common network connectivity issues in an enterprise environment.

---

# IPv4 Address

## Purpose

An IPv4 address uniquely identifies a device on a network and allows it to communicate with other devices.

### Example

```
192.168.1.157
```

### Common Uses

- Identify a workstation on the network.
- Verify a device has received a valid IP address.
- Troubleshoot connectivity issues.

### When to Use

- User reports no network connectivity.
- Verify IP address assignment.
- Diagnose DHCP-related issues.

---

# Private vs Public IP Addresses

## Private IP Address

Private IP addresses are used inside local networks and cannot be accessed directly from the internet.

### Common Private IP Ranges

- 10.0.0.0 – 10.255.255.255
- 172.16.0.0 – 172.31.255.255
- 192.168.0.0 – 192.168.255.255

---

## Public IP Address

A public IP address is assigned by an Internet Service Provider (ISP) and allows communication over the internet.

---

# Subnet Mask

## Purpose

A subnet mask identifies which portion of an IP address belongs to the network and which portion identifies the host.

### Example

```
255.255.255.0
```

### When to Use

- Verify devices are on the correct network.
- Troubleshoot communication between devices.

---

# Default Gateway

## Purpose

The default gateway is the router that forwards traffic from the local network to other networks, including the internet.

### Example

```
192.168.1.1
```

### When to Use

- User cannot access internet resources.
- Verify routing configuration.

---

# DHCP (Dynamic Host Configuration Protocol)

## Purpose

DHCP automatically assigns network configuration settings to client devices.

### Automatically Assigns

- IP Address
- Subnet Mask
- Default Gateway
- DNS Server

### When to Use

- Computer receives an APIPA address (169.254.x.x).
- User has no internet connection.
- IP configuration problems are suspected.

---

# DNS (Domain Name System)

## Purpose

DNS translates domain names into IP addresses.

### Example

```
google.com

↓

142.251.x.x
```

### When to Use

- Websites cannot be reached by name.
- `ping 8.8.8.8` succeeds but `ping google.com` fails.
- Users report webpage loading failures.

---

# MAC Address

## Purpose

A MAC address is the unique hardware address assigned to a network adapter.

### Example

```
74-D8-3E-1E-12-84
```

### When to Use

- Device identification.
- DHCP reservations.
- Network inventory.
- Troubleshooting duplicate devices.

---

# Windows Networking Tools

---

## ipconfig

### Purpose

Displays the current IP configuration.

### Common Uses

- Verify IP Address
- Verify Default Gateway
- Verify Subnet Mask

### Command

```cmd
ipconfig
```

---

## ipconfig /all

### Purpose

Displays detailed network configuration.

### Shows

- MAC Address
- DHCP Status
- DNS Servers
- Lease Information
- Adapter Details

### Command

```cmd
ipconfig /all
```

---

## ipconfig /release

### Purpose

Releases the current DHCP lease.

### Command

```cmd
ipconfig /release
```

---

## ipconfig /renew

### Purpose

Requests a new IP address from the DHCP server.

### Command

```cmd
ipconfig /renew
```

---

## ping

### Purpose

Tests network connectivity between two devices.

### Example

```cmd
ping google.com
```

or

```cmd
ping 8.8.8.8
```

### When to Use

- Verify internet connectivity.
- Test communication with another device.
- Measure response time.

---

## nslookup

### Purpose

Tests DNS name resolution.

### Command

```cmd
nslookup google.com
```

### When to Use

- Verify DNS functionality.
- Troubleshoot website access issues.

---

## tracert

### Purpose

Displays the path packets take across the network.

### Command

```cmd
tracert google.com
```

### When to Use

- Identify where network communication fails.
- Troubleshoot routing problems.

---

# Standard Network Troubleshooting Workflow

1. Verify physical or Wi-Fi connection.
2. Run `ipconfig` to confirm a valid IP address.
3. Verify the default gateway and DNS server.
4. Ping the default gateway.
5. Ping `8.8.8.8` to test internet connectivity.
6. Ping `google.com` to verify DNS resolution.
7. Run `nslookup` if DNS issues are suspected.
8. Use `tracert` to identify where communication stops.
9. Renew the DHCP lease if necessary.
10. Confirm the issue is resolved with the user.

---

# Estimated Resolution Time

| Task | Estimated Time |
|------|----------------|
| IP Configuration Review | 5–10 minutes |
| DNS Troubleshooting | 10–15 minutes |
| DHCP Lease Renewal | 5 minutes |
| Network Connectivity Testing | 10–15 minutes |
| Route Analysis | 15–20 minutes |

---

# Escalation Criteria

Escalate the issue if:

- Multiple users are affected.
- Network equipment appears offline.
- DHCP server is unavailable.
- DNS server is unreachable.
- Internet outage affects the entire office.
- Administrative access is required.
- The issue persists after completing standard troubleshooting.

---

# Best Practices

- Verify the physical connection before troubleshooting software.
- Gather information before making changes.
- Document all troubleshooting steps.
- Confirm resolution with the user before closing the ticket.
- Escalate issues outside Tier 1 support responsibilities.

---

# Summary

Networking fundamentals are essential for IT Support Specialists because they provide the foundation for diagnosing and resolving connectivity issues. Understanding IP addressing, DHCP, DNS, gateways, and Windows networking tools allows technicians to identify problems quickly, restore network access, and minimize downtime for employees.

---

# Related Knowledge Base Articles

- KB-0001 – Computer Hardware Overview
- KB-0002 – Windows Administration Tools
- LAB-0003 – Network Connectivity Fundamentals
- HD-0003 – No Internet Access