# Help Desk Ticket

**Ticket ID:** HD-0003

**Priority:** High

**Status:** Resolved

**Technician:** Kutbul Wara

**Date:** July 1, 2026

---

# User Information

**Employee:** Sarah Ahmed

**Department:** Finance

**Device:** STS-LT-021

---

# Reported Issue

The user reported that their computer displayed **"No Internet Access"** and they were unable to browse websites, access Microsoft 365 applications, or connect to company resources.

---

# User Interview

The following questions were asked to gather additional information:

- When did the issue begin?
- Are you connected using Wi-Fi or Ethernet?
- Is anyone else experiencing the same issue?
- Have you recently restarted your computer?
- Can you access any internal company resources?
- Have you connected to a different network recently?

### User Responses

- The issue started this morning after signing in.
- The laptop was connected to the office Wi-Fi.
- Other employees nearby had internet access.
- The computer had not been restarted.
- No internal or external websites were accessible.
- No recent network changes were made.

---

# Initial Investigation

The following troubleshooting steps were performed:

- Verified the Wi-Fi connection was active.
- Ran `ipconfig` to review the assigned IP address.
- Ran `ipconfig /all` to verify DHCP and DNS settings.
- Ran `ping 8.8.8.8` to test internet connectivity.
- Ran `ping google.com` to test DNS resolution.
- Ran `nslookup google.com` to verify DNS functionality.
- Reviewed the network adapter status.

---

# Root Cause

The computer had received an **Automatic Private IP Address (APIPA)** because it was unable to obtain a valid IP address from the DHCP server. Without a valid IP address, the workstation could not communicate with the network or access the internet.

---

# Resolution

The following actions were taken:

1. Released the current IP address using `ipconfig /release`.
2. Requested a new DHCP lease using `ipconfig /renew`.
3. Confirmed a valid IP address was assigned.
4. Verified the default gateway and DNS server information.
5. Successfully pinged `8.8.8.8`.
6. Successfully pinged `google.com`.
7. Confirmed internet access was restored.
8. Asked the user to verify access to Microsoft 365 and company websites.

---

# Verification

The user successfully accessed websites, Microsoft 365 applications, and internal company resources after the DHCP lease was renewed. Internet connectivity was fully restored.

---

# Business Impact

The employee was temporarily unable to access cloud-based applications, email, and online financial systems, preventing normal work activities. Restoring network connectivity minimized downtime and allowed the employee to resume work promptly.

---

# Preventive Recommendations

- Ensure DHCP services are monitored regularly.
- Keep network adapter drivers up to date.
- Encourage users to report connectivity issues immediately.
- Verify network equipment health during routine maintenance.
- Document recurring DHCP-related incidents for trend analysis.

---

# Time Spent

25 minutes

---

# Lessons Learned

- Always verify the network connection before assuming a hardware failure.
- `ipconfig` quickly confirms whether the workstation has a valid IP address.
- Comparing `ping 8.8.8.8` with `ping google.com` helps distinguish DNS issues from internet connectivity issues.
- Renewing a DHCP lease can resolve many network connectivity problems.
- A structured troubleshooting approach leads to faster and more accurate issue resolution.

---

# Resolution Verification

The user confirmed stable internet connectivity after the repair. Multiple websites and cloud applications were tested successfully, and no additional connectivity issues were reported.

---

# Status

**Resolved**

---

# Related Documentation

- LAB-0003 – Network Connectivity Fundamentals
- KB-0003 – Networking Fundamentals
- KB-0002 – Windows Administration Tools