# Adverse Event Safety Signal Monitoring

An automated clinical safety analytics pipeline using **SQL**, **R**, and **Power BI** to evaluate adverse event (AE) incidence, statistical significance, and pharmacovigilance disproportionality signals (PRR) on the CDISC SDTM Pilot trial dataset.

## Executive Summary
Analyzed 1,191 AE records across 306 trial subjects (Placebo $n=86$, Low Dose $n=84$, High Dose $n=84$, excluding Screen Failures) to identify drug-related safety signals.

* **Dose-Dependent Incidence:** High Dose (94.0%), Low Dose (91.7%), Placebo (80.2%). High Dose vs. Placebo was statistically significant ($p = 0.014$).
* **6 Flagged Safety Signals:** PRR screening ($\text{PRR} > 2.0$, $n \ge 3$) highlighted local patch reactions (*Application Site Erythema*, *Pruritus*) and systemic cholinergic effects (*Sinus Bradycardia*, *Dizziness*, *Nausea*).
* **Serious Adverse Events:** Identified 3 SAEs (2 High Dose, 1 Low Dose, 0 Placebo).

## Data Pipeline & Workflow
1. **SQL (SQLite):** Aggregated incidence, severity breakdowns, and System Organ Class (SOC) distributions on dosed populations.
2. **R:** Executed Chi-Square tests for incidence rate differences and computed Proportional Reporting Ratios (PRR) for disproportionality screening.
3. **Power BI:** Developed a two-page dashboard featuring executive KPI safety cards and conditional-formatted PRR signal detection tables.

## Tech Stack
* **Database & Aggregation:** SQL (SQLite)
* **Statistical Analysis:** R (Base R Stats)
* **Reporting & Dashboards:** Power BI

## Key Deliverable
An interactive, automated safety review suite translating raw SDTM clinical data into actionable pharmacovigilance signals for clinical trial teams.
