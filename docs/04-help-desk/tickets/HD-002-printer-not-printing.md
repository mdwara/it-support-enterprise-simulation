# Help Desk Ticket

**Ticket ID:** HD-0002

**Priority:** Medium

**Status:** Resolved

**Technician:** Kutbul Wara

**Date:** June 30, 2026

---

# User Information

**Employee:** James Lee

**Department:** Human Resources

**Device:** STS-LT-014

---

# Reported Issue

The user reported that the office printer appeared to be online and ready, but documents sent to the printer were not printing. Print jobs remained in the queue without completing.

---

# User Interview

The following questions were asked to gather additional information:

- When did the issue begin?
- Is this your default printer?
- Are other employees able to print?
- Are there any error messages displayed?
- Is the printer connected through the network or USB?
- Have you restarted your computer or the printer?

### User Responses

- The issue started this morning.
- The correct printer was selected as the default printer.
- Other employees were able to print successfully.
- No error messages were displayed.
- The printer was connected to the office network.
- The user had already restarted the computer.

---

# Initial Investigation

The following troubleshooting steps were performed:

- Verified the printer was online.
- Confirmed the correct printer was selected as the default printer.
- Checked the print queue for stuck print jobs.
- Reviewed the Print Spooler service status.
- Verified the printer driver was installed correctly.
- Reviewed Event Viewer for any print-related errors.

---

# Root Cause

The **Print Spooler** service had unexpectedly stopped after a recent Windows Update. Because the service was not running, Windows was unable to process print jobs, causing documents to remain in the print queue.

---

# Resolution

The following actions were taken:

1. Restarted the Print Spooler service.
2. Cleared all pending print jobs from the print queue.
3. Verified the printer status showed **Online**.
4. Sent a Windows test page.
5. Confirmed the test page printed successfully.
6. Asked the user to print a document.
7. Verified the user's document printed successfully.

---

# Business Impact

The employee was temporarily unable to print Human Resources documents, delaying routine administrative tasks. Restoring the Print Spooler service minimized workflow disruption and allowed normal business operations to resume.

---

# Time Spent

20 minutes

---

# Lessons Learned

- Always verify the Print Spooler service before reinstalling printer drivers.
- Check the print queue for stalled print jobs.
- Confirm the correct default printer is selected.
- Test printing before closing the support ticket.
- Document all troubleshooting steps for future reference.

---

# Resolution Verification

The user successfully printed multiple documents after the Print Spooler service was restarted. Printing functionality was fully restored, and no additional issues were reported.

---

# Status

**Resolved**

---

# Related Documentation

- KB-0002 – Windows Administration Tools
- KB-0001 – Computer Hardware Overview
- LAB-0002 – Windows Administration & Troubleshooting