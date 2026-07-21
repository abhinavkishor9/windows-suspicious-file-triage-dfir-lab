# Investigation Timeline

| Time | Activity | Evidence |
|------|----------|----------|
| 09:00 | Created investigation workspace | PowerShell |
| 09:03 | Created simulated suspicious file | Notepad |
| 09:06 | Reviewed file properties | Windows Explorer |
| 09:10 | Verified digital signature | File Properties |
| 09:13 | Collected metadata using PowerShell | Get-Item |
| 09:16 | Calculated SHA256 hash | Get-FileHash |
| 09:20 | Reviewed file location | Windows Explorer |
| 09:24 | Correlated collected evidence | Documentation |
| 09:30 | Investigation completed | Investigation Notes |

---

# Investigation Flow

Investigation Started

↓

Suspicious File Identified

↓

Metadata Collected

↓

Digital Signature Verified

↓

SHA256 Hash Generated

↓

File Location Reviewed

↓

Evidence Correlated

↓

Initial Risk Assessment Completed

↓

Investigation Closed

---

# Summary

The investigation successfully demonstrated a standard DFIR file triage workflow. Without executing the suspicious file, metadata, digital signature information, cryptographic hashes, and contextual evidence were collected and correlated to perform an initial forensic assessment while preserving evidence integrity.
