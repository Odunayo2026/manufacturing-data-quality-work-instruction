# Manufacturing Production Data Quality Assessment & Work Instruction

## Project Overview
This portfolio simulation demonstrates the development of a controlled Work Instruction for a manufacturing production-data quality assessment workflow. The project combines technical writing, data-quality controls, Python-based validation, traceability, and release-decision documentation.

## Primary Portfolio Deliverable
**WI-DA-001 — Performing Production Data Quality Assessment Using Python**

The Work Instruction guides a trained Data Analyst through:
- verifying the authorized working dataset;
- executing schema, completeness, type, domain, range, timestamp, and cross-field checks;
- reviewing statistical anomalies without automatically deleting them;
- documenting validation issues;
- applying HOLD, REVIEW REQUIRED, or APPROVED disposition logic; and
- preserving validation evidence without altering the original source dataset.

## Project Architecture
```text
data/
├── source/
│   └── production_batch_2026_001.csv
├── working/
│   └── production_batch_2026_001_working.csv
└── reference/
    └── production_data_dictionary.csv

config/
└── validation_rules.yaml

development/
└── defect_manifest.csv

notebook/
└── production_data_quality_assessment.ipynb

outputs/
├── validation_summary.csv
├── validation_issues.csv
├── release_report.csv
└── defect_detection_test_report.csv

visuals/
├── validation_summary_output.png
├── release_output.png
└── disposition_decision_flow.png
```

## Validation Design
The workflow separates four validation layers:
1. **Schema validation** — required fields and structure.
2. **Domain validation** — completeness, data types, allowed values, hard ranges, and timestamp validity.
3. **Cross-field validation** — business relationships between related variables.
4. **Statistical review flags** — unusual observations requiring contextual review but not automatic deletion.

## Controlled Test Scenario
The simulated dataset contains 24,000 manufacturing production records. Controlled defects were intentionally introduced during development so the validation workflow could be tested against known conditions.

The final test detected **56 of 56 controlled defect events (100%)**.

The resulting simulated release decision is **HOLD** because unresolved Critical validation issues are present.

## Technical-Writing Principles Demonstrated
- audience- and task-focused instruction;
- Action → Expected Result → Response structure;
- controlled terminology and role boundaries;
- measurable acceptance criteria;
- source-data preservation;
- traceability from validation rule to issue and disposition;
- distinction between anomalies and confirmed invalid data;
- troubleshooting and exception handling;
- document control and revision history.

## Portfolio Note
This is a fictional professional portfolio simulation. The organization, requirements, document identifiers, dataset, roles, and workflow were created for demonstration purposes and are not an approved procedure for any real company.
