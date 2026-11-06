# InventoryOS — Adaptive Inventory Analytics

**From fragmented inventory data to actionable supply chain decisions.**

InventoryOS is an inventory analytics project designed to help teams transform inconsistent Excel/CSV files into structured inventory insights, identify stock risks, and prioritize actions at the SKU–warehouse level.

**Status:** Functional development prototype | Local testing completed | Live deployment pending validation

## 1. The Problem

Inventory data often comes from different systems, warehouses, and reporting formats. Inconsistent column names, missing fields, and unreliable records make it difficult to assess stock availability and identify inventory risks.

InventoryOS explores a practical question:

**How can supply chain teams turn fragmented inventory records into reliable, actionable planning insights?**

## 2. The Solution

InventoryOS follows a five-stage analytical workflow:

**Import → Map → Validate → Analyze → Prioritize**

- **Flexible Data Import:** Supports Excel/CSV inputs with different layouts and column structures.
- **Column Mapping:** Helps standardize source fields into a consistent data model.
- **Data Quality:** Flags missing values, inconsistent records, duplicates, and suspicious quantities.
- **Inventory Analytics:** Calculates inventory KPIs when the necessary data is available.
- **Action Center:** Highlights SKU–warehouse risks and provides evidence-based recommendations.

## 3. Selected Features

*All images below are genuine InventoryOS development-prototype screenshots using demo/test data. They do not represent live production deployment.*

### Sign-in Experience

The current interface uses email/password sign-in; Supabase connection settings are configured by the application owner, not entered by end users.

![InventoryOS sign-in screen](assets/login.webp)


### Inventory Dashboard

Inventory KPIs and risk indicators can be explored across national, warehouse, and product views.

![InventoryOS Dashboard](assets/dashboard.webp)

### Flexible Column Mapping

Maps non-standard source columns into the InventoryOS analytical structure.

![Column Mapping](assets/column-mapping.webp)

### Data Quality Validation

Identifies records requiring correction, review, or additional information before analysis.

![Data Quality](assets/data-quality.webp)

### Inventory Risk Prioritization

Organizes potential inventory problems into a structured action list.

![Action Center](assets/action-center.webp)

### Dashboard PDF Export

Generates a formatted PDF report for communicating analytical findings.

![PDF Dashboard](assets/pdf-report.webp)

## 4. Technical Approach

For a concise overview of the processing flow and KPI availability rules, see [Architecture](docs/architecture.md) and [KPI Methodology](docs/kpi-methodology.md).


**Frontend:** JavaScript, HTML, CSS

**Data processing:** Excel/CSV parsing, field normalization, validation, and inventory KPI calculations

**Backend architecture:** Supabase PostgreSQL, Authentication, and Row Level Security

**Additional integration:** Google Apps Script for the development workflow

The application follows a data pipeline from source files to standardized records, analytical KPIs, and prioritized inventory actions.

## 5. Validation and Limitations

Local testing has covered sample data imports, column mapping, data-quality checks, KPI reconciliation, duplicate detection, and PDF generation.

The application is under development. Live Supabase integration, authentication permissions, and production operations require further end-to-end validation.

All screenshots and figures presented here are from a demonstration environment and do not represent actual company operating results.

## 6. Project Scope

This public repository presents selected project documentation, interface screenshots, and analytical methodology.

The full application source code, deployment configuration, and operational database are not included.

---

**Project focus:** Inventory Analytics · Supply Chain Planning · Data Quality · Decision Support
