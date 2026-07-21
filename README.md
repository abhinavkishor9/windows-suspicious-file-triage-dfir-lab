# windows-suspicious-file-triage-dfir-lab
## Overview

This Digital Forensics and Incident Response (DFIR) lab demonstrates how to safely perform an initial triage of a suspicious file using native Windows forensic artifacts and utilities.

Rather than executing an unknown file, investigators first collect evidence such as metadata, cryptographic hashes, digital signature information, and file location to determine whether the file warrants further malware analysis.

---

# Executive Summary

This investigation demonstrates the standard DFIR workflow for analyzing a suspicious file while preserving evidence. A simulated suspicious executable was created for training purposes and investigated using Windows File Properties, PowerShell, and native hashing utilities.

The investigation focused on metadata collection, digital signature verification, SHA256 hash generation, and evidence correlation to determine whether the file exhibited characteristics requiring further investigation.

---

# Learning Objectives

- Understand the purpose of file triage.
- Safely investigate suspicious files without execution.
- Examine Windows file metadata.
- Verify digital signatures.
- Calculate SHA256 file hashes.
- Assess suspicious indicators.
- Document forensic findings.

---

# Skills Demonstrated

- Windows DFIR Investigation
- Suspicious File Triage
- File Metadata Analysis
- Digital Signature Verification
- SHA256 Hash Calculation
- File Integrity Validation
- Evidence Preservation
- IOC Identification
- Evidence Correlation
- Digital Evidence Documentation
- MITRE ATT&CK Mapping

---

# Tools Used

- Windows Explorer
- File Properties
- Windows PowerShell
- Get-Item
- Get-FileHash
- Notepad

---

# Lab Environment

| Component | Details |
|-----------|---------|
| Operating System | Windows 10 / Windows 11 |
| Investigation Type | Digital Forensics |
| Utilities | Native Windows Tools |
| Sample File | Simulated Executable |
| Hash Algorithm | SHA256 |
| Internet Required | No |

---

# Investigation Scenario

The SOC receives an alert that a suspicious executable named **Invoice_Update.exe** has been discovered on a user workstation.

As the assigned DFIR analyst, your objectives are to determine:

- File metadata
- File location
- Digital signature status
- SHA256 hash
- Initial risk assessment
- Whether escalation is required

The file is **not executed** during this investigation.

---

# Investigation Workflow

1. Create investigation workspace.
2. Create simulated suspicious file.
3. Examine Windows file properties.
4. Verify digital signature.
5. Collect metadata using PowerShell.
6. Calculate SHA256 hash.
7. Review file location.
8. Correlate collected evidence.
9. Document findings.

---

# MITRE ATT&CK Mapping

| Tactic | Technique | ID |
|---------|-----------|----|
| Discovery | File and Directory Discovery | T1083 |
| Collection | Data from Local System | T1005 |

### Why File Triage Matters

Initial file triage is one of the first steps performed during incident response. Analysts avoid executing unknown files and instead collect metadata, hashes, signatures, and contextual information to determine whether deeper malware analysis is necessary.

---

# Evidence Collected

- File Properties
- File Name
- File Size
- File Location
- Created Time
- Modified Time
- Last Access Time
- Digital Signature Status
- SHA256 Hash
- PowerShell Metadata

---

# Evidence Correlation

| Evidence Source | Information Obtained | Investigation Value |
|-----------------|---------------------|--------------------|
| File Properties | Basic metadata | Initial assessment |
| PowerShell Get-Item | MAC Times | Metadata validation |
| Get-FileHash | SHA256 fingerprint | Integrity verification |
| Digital Signature | Trust validation | Authenticity assessment |
| File Location | Storage path | Contextual evidence |

Correlating multiple evidence sources allows investigators to perform an accurate initial assessment while maintaining forensic integrity.

---

# Investigation Findings

- Simulated suspicious executable successfully examined.
- Metadata collected without executing the file.
- SHA256 hash generated for integrity verification.
- No digital signature was present.
- File location reviewed as part of contextual analysis.
- Evidence supported an initial triage assessment without requiring execution.

---

# Key Takeaways

- Unknown files should never be executed during initial DFIR investigations.
- Metadata provides valuable contextual evidence.
- Digital signatures help assess software authenticity.
- SHA256 hashes uniquely identify files.
- Multiple artifacts should always be correlated before reaching investigative conclusions.

---

