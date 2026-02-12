# Hardware-Projects-Troubleshooting

## Overview: Advanced Hardware IT Support Report
[cite_start]This project documents the troubleshooting and repair process for a custom-built desktop that experienced a total boot failure[cite: 8, 31]. [cite_start]The repository serves as a case study for identifying and resolving motherboard BIOS corruption using advanced hardware workarounds[cite: 28, 34].

---

## System Specifications
[cite_start]The following components were utilized in the system under repair[cite: 21]:

* [cite_start]**CPU:** Ryzen 5 2600x [cite: 22]
* [cite_start]**GPU:** PNY GTX 1650 Super [cite: 22]
* [cite_start]**Motherboard:** MSI x470 (Featuring EZ Debug LEDs) [cite: 23, 27]
* [cite_start]**RAM:** XPG 2x8GB DDR4 [cite: 23]
* [cite_start]**PSU:** EVGA BR 550W [cite: 24]
* [cite_start]**Storage:** NVME Gen 3 500GB [cite: 25]

---

## The Problem
**Reported Issue:** The system functioned normally before suddenly freezing. [cite_start]Upon attempting a restart, the computer failed to boot (No POST)[cite: 26]. 

### Initial Findings
* [cite_start]**Visual Check:** Lights were visible, but no image was produced on the display[cite: 26, 27].
* [cite_start]**Initial Theory:** Suspected OS corruption or a localized hardware failure[cite: 27].

---

## Troubleshooting Methodology
[cite_start]A systematic approach was taken to isolate the failing component[cite: 27, 28]:

| Component | Test Performed | Result |
| :--- | :--- | :--- |
| **Power Supply** | [cite_start]Tested with a dedicated PSU tester and secondary system[cite: 27]. | [cite_start]**Passed:** Proper voltage confirmed[cite: 28]. |
| **RAM** | [cite_start]Swapped modules and tested in a functional system[cite: 27, 28]. | [cite_start]**Passed:** RAM functioned normally elsewhere[cite: 27]. |
| **GPU** | [cite_start]Installed a different GPU in the customer's PC; tested original GPU elsewhere[cite: 27, 28]. | [cite_start]**Passed:** The original GPU worked fine; the PC still failed to boot with a new card[cite: 27]. |
| **Motherboard** | [cite_start]Analyzed EZ Debug LED error codes (RAM and Video errors)[cite: 27]. | [cite_start]**Failed:** Issues persisted even after CMOS reset[cite: 28]. |

---

## Diagnosis & Resolution
### The Root Cause
[cite_start]The boot failure was definitively attributed to **corrupted BIOS** on the MSI x470 motherboard[cite: 31].

### The Solution
[cite_start]Since the motherboard lacked a dedicated "USB Flash" button for headless updates, the following workaround was implemented[cite: 28]:
1.  [cite_start]**CPU Swap:** Installed a temporary CPU with integrated graphics to bypass the VGA POST error[cite: 28, 34].
2.  [cite_start]**BIOS Access:** Successfully gained access to the BIOS interface using the integrated graphics[cite: 34].
3.  [cite_start]**Firmware Update:** Updated the BIOS to the latest stable version[cite: 35].
4.  [cite_start]**System Restoration:** Reinstalled the original Ryzen 5 2600x and GTX 1650 Super[cite: 35].

[cite_start]**Result:** The system passed POST and booted into the OS normally[cite: 36].

---

## Key Takeaways: BIOS Corruption
[cite_start]This project highlights several common factors that can lead to BIOS instability[cite: 37]:
* [cite_start]**Power Instability:** Surges or fluctuations during operation[cite: 37].
* [cite_start]**Failed Updates:** Interrupted firmware flashes[cite: 37].
* [cite_start]**Environmental Factors:** Overheating or electrical faults[cite: 37].

---

## Credits
* [cite_start]**Technician:** Luz E Cabrera Rios [cite: 2]
* [cite_start]**Course:** CIS-472: Advanced Hardware [cite: 4]
* [cite_start]**Institution:** Wayne State College [cite: 3]
* [cite_start]**Instructor:** Jeremy Wynia [cite: 5]
