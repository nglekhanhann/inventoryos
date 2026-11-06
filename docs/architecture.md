# InventoryOS — Architecture Overview

**Scope:** Development prototype, not a production deployment or public source release.

## Processing pipeline

1. **Import** spreadsheet/CSV exports with different headers and layouts.
2. **Column mapping** associates source fields with canonical inventory fields.
3. **Data quality** checks missing identifiers, invalid or outlying quantities, duplicates, and inconsistent records; issues are surfaced for review.
4. **Standardization** prepares SKU–warehouse data for analysis, with a Supabase/PostgreSQL persistence architecture.
5. **Analytics** derives inventory KPIs only when required source data exists.
6. **Prioritization** lists actionable inventory risks and review candidates by SKU and warehouse.
7. **Communication** supports dashboard views and PDF/CSV exports.

## Architecture boundaries

- **User interface:** HTML, CSS, JavaScript; email/password sign-in in the cloud setup.
- **Data model:** PostgreSQL/Supabase organization-aware records and authorization policies.
- **Integration option:** Google Apps Script supports an owner-only development deployment.
- **Deployment status:** Local demonstration and tests have been performed; live production end-to-end acceptance remains pending.

This public repository intentionally excludes full application source, Supabase configuration, access credentials, operational data, and migration scripts.
