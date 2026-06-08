# GCP Cloud Spanner Studio

This repository contains the target configuration and SRE runtime files compiled by the **GCP Cloud Spanner Studio** dashboard module.

## 🚀 Description
Design globally distributed Cloud Spanner SQL schemas. Generate instance configurations, DDL database setups, and optimized database session pool limits.

## 🛠️ Specification Matrix
- **Primary Configuration File**: `/db/spanner/spanner_ddl.sql`
- **Execution Command**: `gcloud spanner databases ddl update db --instance=inst --ddl-file=spanner_ddl.sql`
- **Validation Command**: `gcloud spanner databases ddl describe db --instance=inst`

## 📋 How to Run & Validate

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Pradeeptalari14/tp-gcp-cloud-spanner.git
   cd tp-gcp-cloud-spanner
   ```

2. **Run Execution Target:**
   ```bash
   gcloud spanner databases ddl update db --instance=inst --ddl-file=spanner_ddl.sql
   ```

3. **Verify Runtime Stability:**
   ```bash
   gcloud spanner databases ddl describe db --instance=inst
   ```

## 🔐 Security & Best Practices
* **Secret Isolation**: Use organization-level secrets (or SSM parameter hooks) rather than hardcoded environment variables inside files.
* **Pull Request Lifecycles**: Protect default branch merges with validation checks before merging code changes.
