# Linux Access Control Enforcement 
## File Permission Audit

### Overview

I performed a security audit of file and directory permissions within a Linux environment `(/home/researcher2/projects)` to identify and remediate access control weaknesses.

The objective was to enforce the principle of least privilege by removing excessive permissions and restricting access to sensitive resources. This project demonstrates how technical access controls can reduce security risk and support broader governance and compliance objectives. 

### Initial Environment

The /home/researcher2/projects directory contained several files and one subdirectory with inconsistent and overly permissive access settings.

Key issues identified in the initial environment included:

- `project_k.txt` allowed read and write access for owner, group, and others
- `project_r.txt` and `project_t.txt` allowed group write access
- `project_x.txt` had inappropriate permissions for a hidden archived file
- the `drafts` directory allowed group execute access, creating unnecessary directory exposure

This initial state introduced risks related to unauthorised modification, excessive permissions, and avoidable access to sensitive content.

### Assessment and Findings

Using the command below, I reviewed all files in the directory, including hidden files:

```bash
ls -la /home/researcher2/projects
```

![Initial permission audit using ls -la](images/permissions-audit-ls-la.png)

Using `ls -la`, I reviewed both visible and hidden files to identify excessive permissions and access control weaknesses.

The review identified the following issues:

### Excessive Permissions

Some files had overly permissive access settings. For example:

```bash
-rw-rw-rw- project_k.txt
```

This created a risk of unauthorised modification and weakened data integrity.

### Inconsistent Access Control

Some files had permissions such as:

```bash
-rw-rw-r-- project_r.txt
```

This granted unnecessary group write access and was not aligned with least privilege.

### Directory Exposure

The `drafts` directory had permissions such as:

```bash
drwx--x--- drafts
```
This allowed unnecessary directory traversal and increased exposure to sensitive content.

### Remediation Actions

To remove unnecessary write access and standardise permissions across files, I used:

```bash
chmod 644 project_k.txt project_r.txt project_t.txt
```

This ensured that:

- the owner retained read and write access
- group access was reduced to read only
- others were limited to read only
- Secured Sensitive Hidden File

To protect the archived hidden file, I used:

```bash
chmod 440 .project_x.txt
```

This ensured that:

- the owner and group had read-only access
- others had no access
- Restricted Directory Access

To restrict the `drafts` directory so that only the owner could access it, I used:

```bash
chmod 700 drafts
```

This ensured that:

- the owner had full access
- group and others had no access

### Verification of Corrected Permissions

After applying the permission changes, I re-ran `ls -la` to confirm that the files and directory permissions were corrected and aligned with least privilege principles.

![Corrected file permissions after remediation](images/permissions-after-remediation.png)

### Security Impact

These remediation actions:

- reduced the risk of unauthorised modification
- protected sensitive research data
- strengthened enforcement of access control policies
- improved system integrity and auditability

### GRC Alignment

This project demonstrates how technical controls support broader governance, risk, and compliance objectives, including:

- enforcement of least privilege
- reduction of access control risk
- alignment with role-based access control principles
- practical implementation of security policy enforcement

### Summary

By auditing and correcting file permissions, I transformed a misconfigured environment into one aligned with secure access control practices. This reduced both operational and compliance risk while demonstrating hands-on ability to assess and remediate permission-based security issues in Linux.
