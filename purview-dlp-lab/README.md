# Purview DLP Lab

**What it does**  
Demonstrates a minimal DLP policy definition captured via export, with redactions, and a rollout plan:
1) **Test** in simulation (policy tips only)  
2) **Audit** actions (report-only)  
3) **Block with override** for specific roles/groups

**How to get JSON (in a real tenant)**
- Use Security & Compliance/Exchange Online PowerShell:
  - `Export-DlpPolicyCollection -Identity "All" | Set-Content .\dlp-export.json`
  - Redact/trim before committing.

**Import (lab)**  
- `Import-DlpPolicyCollection -FileData ([System.IO.File]::ReadAllBytes("dlp-export.json"))`


