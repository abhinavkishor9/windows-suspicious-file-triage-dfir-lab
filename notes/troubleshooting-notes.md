# Troubleshooting Notes

## Issue 1 — File Extension Hidden

### Cause

Windows hides known file extensions by default.

### Resolution

Enable **View → File name extensions** in File Explorer before renaming files.

---

## Issue 2 — Unable to Rename to .exe

### Cause

File extensions remain hidden.

### Resolution

Enable file extensions and rename the complete filename.

---

## Issue 3 — Digital Signature Tab Missing

### Cause

Unsigned files do not contain a Digital Signatures tab.

### Resolution

This is expected behavior. Record the absence of a signature as part of the investigation.

---

## Issue 4 — SHA256 Hash Changes

### Cause

Any modification to file contents changes the cryptographic hash.

### Resolution

Recalculate the hash after any modification.

---

## Issue 5 — PowerShell Metadata Appears Different

### Cause

PowerShell displays timestamps using regional system settings.

### Resolution

Compare timestamp values rather than formatting.

---

# Lessons Learned

- Unknown files should not be executed during initial triage.
- Metadata should be collected before any interaction with the file.
- SHA256 hashes uniquely identify files.
- Digital signatures assist in validating software authenticity.
- Evidence correlation improves investigative confidence.
