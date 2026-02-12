# Hardware-Projects-Troubleshooting

## Overview: Advanced Hardware IT Support Report
This project documents the diagnostic and repair process for a custom-built desktop that experienced a boot failure. The troubleshooting was performed as part of the CIS-472: Advanced Hardware course at Wayne State College.

---

## System Specifications
The following components were analyzed during the repair process:

* **CPU:** Ryzen 5 2600x
* **GPU:** PNY GTX 1650 Super
* **Motherboard:** MSI x470
* **RAM:** XPG 2x8GB DDR4
* **PSU:** EVGA BR 550W
* **Storage:** NVME Gen 3 500GB

---

## The Problem
**Reported Issue:** The computer froze during normal operation and failed to pass POST (Power-On Self-Test) upon restart. 

### Diagnostics & Findings
* **Power Supply:** Verified as functional using a dedicated PSU tester and secondary system.
* **RAM & GPU:** Both components were cross-tested in separate functional systems and confirmed to be working.
* **Motherboard:** The "EZ debug" LEDs indicated specific errors related to RAM and Video, though these components were verified as functional in an external system.



---

## Resolution: BIOS Recovery
### The Root Cause
The failure was identified as **corrupted BIOS** on the motherboard. Because the board lacked a "Flash BIOS" button, a specific hardware workaround was required.

### Actions Taken
1. **Integrated Graphics Workaround:** A CPU with integrated graphics was temporarily installed to bypass the VGA error and gain access to the BIOS interface.
2. **Firmware Update:** Once access was gained, the BIOS was successfully updated to the latest version.
3. **Component Reinstallation:** The original Ryzen 5 2600x and GTX 1650 Super were reinstalled.

**Result:** The system passed POST successfully and booted normally into the operating system.

---

## Technical Credits
* **Technician:** Luz E Cabrera Rios
* **Department:** Computer Technology and Information Systems, Wayne State College
* **Instructor:** Jeremy Wynia
* **Date:** April 1, 2025
