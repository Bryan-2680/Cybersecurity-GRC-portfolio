### Linux File Permission Audit
A hands-on Linux exercise reviewing and remediating file and directory permissions to enforce least privilege at the command line.

#### What it demonstrates

- Reviewing permissions with ls -la, including hidden files
- Remediating with chmod (e.g. 644 for files, 440 for a sensitive hidden file, 700 for an owner-only directory)
- Verifying the corrected state rather than assuming the change worked
- Understanding Unix discretionary access control (DAC) and how it differs from role-based access control (RBAC), while serving the same least-privilege objective

#### Key concepts: least privilege, file permissions, chmod notation (read=4 / write=2 / execute=1), DAC vs RBAC, remediation and verification.

Hands-on lab exercise (Google Cybersecurity Certificate). Included to demonstrate practical command-line ability, not a production system.
