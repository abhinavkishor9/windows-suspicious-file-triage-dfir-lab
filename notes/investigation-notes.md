# Investigation Notes

## Lab Summary

This investigation focused on performing an initial forensic triage of a suspicious file using native Windows utilities. The file was analyzed without execution by examining metadata, digital signatures, cryptographic hashes, and contextual evidence before documenting investigative findings.

---

## Analyst Methodology

The investigation followed a structured DFIR workflow:

1. Create investigation workspace.
2. Create a simulated suspicious file.
3. Review Windows file properties.
4. Verify digital signature information.
5. Collect metadata using PowerShell.
6. Generate SHA256 hash.
7. Assess file location.
8. Correlate collected evidence.
9. Document investigative findings.

---

## Investigation Scenario

A suspicious executable named **Invoice_Update.exe** was reported on a Windows workstation.

The investigation aimed to determine:

- File metadata
- Digital signature status
- SHA256 hash
- File location
- Initial risk assessment

The file was **not executed** during the investigation.

---

## Evidence Collected

### Evidence 1 – Windows File Properties

Collected:

- File Name
- Size
- Created Time
- Modified Time
- Last Access Time

Finding:

Provided the initial forensic baseline.

---

### Evidence 2 – Digital Signature

Collected:

- Signature status

Finding:

No digital signature was present, increasing the need for additional validation.

---

### Evidence 3 – PowerShell Metadata

Command Used

```
Get-Item Invoice_Update.exe
```

Collected:

- CreationTime
- LastWriteTime
- LastAccessTime
- File Length

Finding:

PowerShell validated Windows Explorer metadata.

---

### Evidence 4 – SHA256 Hash

Command Used

```
Get-FileHash Invoice_Update.exe
```

Collected:

- SHA256 fingerprint

Finding:

Generated a unique identifier suitable for IOC tracking and future comparison.

---

## DFIR Analysis

The suspicious file was investigated without execution.

Evidence demonstrated:

- File metadata collection
- Digital signature verification
- Hash generation
- Evidence preservation

Multiple Windows artifacts provided consistent forensic evidence.

---

## MITRE ATT&CK Mapping

| Tactic | Technique | ID |
|---------|-----------|----|
| Discovery | File and Directory Discovery | T1083 |
| Collection | Data from Local System | T1005 |

---

## Analyst Observations

- The file remained unopened throughout the investigation.
- Metadata collection did not modify the file.
- PowerShell confirmed Windows Explorer metadata.
- No digital signature was identified.
- SHA256 hashing established a reliable file fingerprint.
- Evidence correlation supported an initial triage assessment.

---

## Conclusion

The investigation successfully demonstrated the standard DFIR process for suspicious file triage. By collecting metadata, validating signatures, calculating hashes, and correlating evidence without executing the file, the investigation preserved forensic integrity while providing sufficient information for an initial risk assessment. m
