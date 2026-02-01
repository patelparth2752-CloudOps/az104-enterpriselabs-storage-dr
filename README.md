# Enterprise AZ-104 Storage & Disaster Recovery Project

## Overview
This project demonstrates Azure Administrator (AZ-104) skills by designing, deploying, and securing storage solutions with backup and disaster recovery strategies using Azure best practices.

---

## Architecture
- Resource Group: `rg-az104-storage-dr`
- Storage Account: `staz104dr01`
  - Blob Container: `app-data`
  - File Share: `sharedfiles`
  - Soft delete enabled
  - Lifecycle management rules applied
- Recovery Services Vault: `rsv-az104-backup`
  - Backup Azure File Share
  - Retention policy: default (daily)
- Disaster Recovery:
  - Restore individual files
  - Restore entire file share
  - Soft delete recovery

---

## Services Used
- Azure Storage Account (Blob & File Share)
- Recovery Services Vault
- Soft Delete & Lifecycle Management
- RBAC for Storage Access
- Azure Portal / CLI

---

## Security Controls
- Public access enabled for PoC
- RBAC: Storage Blob Data Contributor
- Soft delete enabled for accidental deletion protection

---

## Backup & DR Strategy
- Azure File Share backup via Recovery Services Vault
- Soft delete for blobs and files
- Lifecycle management rules for cost optimization

---

## Restore Scenarios
1. Delete a file in `sharedfiles`
2. Restore from Recovery Services Vault
3. Delete a blob in `app-data`
4. Restore from soft delete

---

## Cost Optimization
- Lifecycle rules move old blobs to Cool tier
- Automated deletion for aged files

---

## Learnings
- Azure Storage configuration and security
- Recovery Services Vault usage
- Backup and restore strategies
- Soft delete vs backup concepts
- Lifecycle management and cost optimization
