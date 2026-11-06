# InventoryOS — KPI Methodology

The prototype uses **data-availability-first reporting**: a KPI should not be displayed as a definitive number without the required fields.

| KPI / analytic view | Minimum data needed | Interpretation / constraint |
| --- | --- | --- |
| On-hand Stock | Valid SKU, warehouse, as-of date, quantity | Recorded stock at the chosen point in time; unit of measure must be consistent. |
| Usable / Available Stock | On-hand and relevant reserved, blocked, or other availability inputs | Report N/A if the availability components cannot be established reliably. |
| Inventory Value | Quantity plus a trustworthy unit cost/valuation basis | Missing cost means N/A, not zero. |
| Days of Supply (DOS) | Usable stock and valid average daily demand | Undefined when demand is unavailable or unsuitable; state the reason. |
| Stockout / replenishment risk | Stock, demand, and/or lead-time context depending on the rule | Treat alerts as decision-support signals, not automatic purchase orders. |

**Data-quality controls:** missing identifiers, duplicates, negative quantities, unexpected magnitudes, incompatible units, and inconsistent dates are flagged for investigation. Issues may be classified by severity before records are accepted.

**Reporting principle:** if an essential input is missing, show **N/A and a clear reason** rather than fabricating a metric.

All screenshots and numeric examples in this repository are demonstration/test data, not company results.
